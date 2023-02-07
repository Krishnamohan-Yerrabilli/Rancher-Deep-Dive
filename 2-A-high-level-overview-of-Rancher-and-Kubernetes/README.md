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




