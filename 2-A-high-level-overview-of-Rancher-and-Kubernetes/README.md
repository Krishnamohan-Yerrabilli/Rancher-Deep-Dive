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

The traditional process of building a K8s cluster, known as "K8s the hard way," can be complicated and change over time. It involves generating a root CA key, configuring etcd, installing kube-apiserver, kube-controller-manager, and kubescheduler, and joining worker nodes to the cluster. 

Rancher aimed to make building K8s clusters easier through its container clustering software, Cattle, in Rancher v1.6. Everything needed to run as a container.

So guys to explain in simple terms "RKE" is Rancher's cluster 'orchestration' basically its a command line tool for creating and managing Cloud Native Computing Foundation (CNCF)-certified K8s clusters with various operating systems and configurations. The core idea of RKE is that everything that makes up the K8s cluster should run inside Docker containers. This allows RKE to be deployed on any 'operating system' as long as it's within a 'Docker container', as RKE does not install binaries on the host or configure services on the 'host system'.

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






