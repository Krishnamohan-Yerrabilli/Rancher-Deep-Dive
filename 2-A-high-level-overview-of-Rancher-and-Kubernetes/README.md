<div align="center">

# A High level overview of Rancher and Kubernetes

</div>

This section will cover the high-level processes of Rancher, Rancher Kubernetes Engine (RKE), RKE2 (also known as `RKE Government`), 
K3s, and RancherD. We will discuss the core design philosophy of each of these products and explore the ways in which they are different. 
We'll dive into `Rancher's` high-level architecture and see how `Rancher server pods` communicate with downstream clusters using the 
`Cattle agents`, which include both the `Cattle-cluster-agent` and the `Cattle-node-agent`. We'll also look at how the `Rancher server` 
uses `RKE` and how `Rancher-machine` provisions downstream nodes and `Kubernetes (K8s)` clusters. After that, we'll cover the high-level 
architecture of `K8s`, including `kube-api-server`, `kube-controller-manager`, and `kube-scheduler`. We'll also discuss how each of these 
components maintains the state of the cluster. Finally, we'll examine how an end user can change the desired state and how the controllers 
can update the current state.

# In this section, we'll discuss:

- The purpose of the `Rancher server`
- What `RKE` and `RKE2` are
- An explanation of `RKE`
- An explanation of `RKE2`
- What `K3s` is
- The role of `RancherD`
- The controllers running inside `Rancher server` pods
- The function of `Cattle agents`
- How `Rancher` manages nodes and clusters
- An overview of `kube-apiserver`, `kube-controller-manager`, `kube-scheduler`, `etcd`, and `kubelet`
- How the `current state` and `desired state` work together
- A summary

# What is the Rancher server?

The `Rancher server` is considered the core of the Rancher ecosystem and contains all necessary components, products, or tools that connect to it via the `Rancher API`. The term "Rancher" is often used interchangeably with the "Rancher server". 

The central component of Rancher is the `Rancher API`, which is built on a custom API framework called `Norman`. This framework acts as a translation layer between the Rancher API and the `K8s API`. All communication in Rancher, including the `Rancher UI` which is 100% API-driven, utilizes the Rancher or K8s API.

Accessing the `Rancher API` is possible through a standard RESTful API. Requests are sent from an external HTTP or TCP load balancer to the ingress controller, then routed to one of the Rancher server pods. `Norman` translates the request into a K8s request, which calls a `CustomResource` object. Since everything is stored in a `CustomResource` object in K8s, the Rancher request flow is stateless and does not require session persistence. 

When a `CustomResource` object is created, changed, or deleted, the corresponding object type's controller takes over and processes the request. This topic will be explored in further detail later in this section.

# RKE and RKE2 are solutions for building a Kubernetes (K8s) cluster. 

Building a `Kubernetes` cluster using the traditional method, known as `K8s the hard way`, can be challenging due to its complexity and the need for constant updates. This process involves generating a root CA key, configuring `etcd`, installing `kube-apiserver`, `kube-controller-manager`, and `kube-scheduler`, and joining worker nodes to the cluster.

To simplify this process, Rancher introduced `RKE` with its container clustering software, `Cattle`, in Rancher v1.6. `RKE` is a command-line tool for creating and managing `CNCF`-certified `Kubernetes` clusters across various operating systems and configurations. The core idea behind `RKE` is to run everything that makes up a `Kubernetes` cluster inside `Docker` containers, which allows `RKE` to be deployed on any operating system as long as it's inside a `Docker` container. This means that `RKE` does not install binaries on the host or configure services on the host system.


```s
user: root
hostname_override: host_01
internal address: 172.27.7.21
role: [controlplane, worker, etcd]
address: 172.27.7.22

user: root
hostname_override: host_02
internal_address: 172.27.7.22
role: [controlplane, worker,etcd]
address: 172.27.7.23

user: root
hostname_override: host_03
internal_address: 172.27.7.23
role: [controlplane, worker, etcd]

services:
  etcd:
    dns:
      backup_config:
        enabled: true
        interval_hours: 12
        retention: 6
        access_key: "ABCDEFGHIJKLMNPO..."
        secret_key: "123456789abcdefghijklmpo....
        bucket_name: "etcd-backups"
        folder: "Cluster-Name-Here"
        endpoint: "s3.us-west-1.mohan.com"
        region: "us-west-1"
        provider: coredns.
        upstreamnameservers:
          - 172.27.2.23
          - 172.27.2.24
```

# Summary

- RKE is Rancher's cluster orchestration tool for creating and managing K8s clusters.
- The core concept of RKE is that everything in the K8s cluster runs within Docker containers, allowing it to run on any operating system.
- RKE uses a configuration file `cluster.yml` to create containers for the components of the K8s cluster (etcd, kube-apiserver, kube-controller-manager, kube-scheduler, and kubelet).

# Explanation of RKE2

RKE2 is Rancher's next-generation `Kubernetes` solution, also known as RKE Government. It was specifically designed to meet the unique requirements of the US federal government and its customers. With RKE2, security is a top priority and is built into the solution by default, making it highly secure with little to no action required by the cluster administrator.

RKE2 is a fully `CNCF`-certified Kubernetes distribution and is built on `K3s`, which brings in the easy setup methods from `K3s` and supports `ARM64`-based systems. This means that RKE2 can be set up on a `Raspberry Pi` or mixed and matched with `AMD64` nodes in the same cluster, providing users with the flexibility to run workloads on low-power and cost-effective `ARM64` nodes. Additionally, RKE2 inherits several features from `K3s`, such as support for multiple arch builds using the `Drone Continuous Integration` (CI) platform.

It has inherited several features from `K3s`, including self-bootstrapping, built-in `Helm` support, and the move from `Docker` to `containerd`. With the self-bootstrapping feature, RKE2 allows nodes to join the cluster using a `registration endpoint` running on the `master nodes`, eliminating the need to define the cluster as `YAML` and use the `RKE binary`. This feature requires an external `load balancer` or a `round-robin DNS` record to be successful.

RKE2 also offers built-in `Helm` support, which was designed with Rancher's fleet feature in mind, where all `cluster services` should be deployed in an automated process using `Helm`. The significant change from `RKE` to RKE2 was the move from `Docker` to `containerd`, which allows the `core Kubernetes components`, such as `etcd` and `kube-apiserver`, to be managed as `static pods` directly by `kubelet` instead of `kube-controller-manager` or `kube-scheduler`. This means that the core components can be viewed and managed just like any other `pod` in the cluster.

# What `K3s` is?

K3s is a fully CNCF-certified `K8s` distribution, designed to run on edge devices where physical space, power, and compute resources are limited. K3s was created as a smaller alternative to traditional `K8s` clusters, which require significant resources to run. 

The core components of K3s, including `kube-apiserver`, `kube-controller-manager`, `kube-scheduler`, and `kubelet`, are merged into a single binary, reducing the overall size and memory footprint of the cluster. `Etcd` is replaced with a database adapter such as SQLite3, which functions as an etcd database but with a smaller CPU and memory usage. 

K3s also eliminates the in-tree storage drivers and cloud providers found in upstream K8s, reducing the overhead and allowing the cluster to fit on a 40 MB binary file and run on a node with only 512 MB of RAM. The optimizations in K3s allow it to stay up to date with upstream K8s without customizing any of the standard K8s libraries in the core components.
