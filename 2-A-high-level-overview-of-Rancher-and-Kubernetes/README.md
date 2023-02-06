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

