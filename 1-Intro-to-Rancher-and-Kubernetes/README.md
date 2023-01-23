# Introduction to Rancher and Kubernetes

Hey guys, in this section we're going to focus on the `history` of `Rancher` and `Kubernetes`. We'll cover the products and solutions that came before them and how they've evolved into what they are today. By the end of this section, you should have a good understanding of the origins of `Rancher` and `Kubernetes` and their `core concepts`. This knowledge is essential for you to understand why `Rancher` and `Kubernetes` are what they are. Let's dive into these topics one by one.-

## In this section, we'll discuss:

- The `background` of `Rancher Labs`
- Rancher's earlier products
- Rancher's main `philosophy`
- The `origins` of `Kubernetes`
- The problem that `Kubernetes` is trying to solve
- How `Kubernetes` compares to `Docker Swarm` and `OpenShift`


#  The background of Rancher Labs

- Rancher Labs was founded in 2014 with the goal of creating a `container management platform` that was `open source` and `community-driven`.
- Rancher is the `flagship product` of Rancher Labs and is used to `manage` and `orchestrate` `containerized workloads` on-premises and in the `cloud`.
- Rancher is `vendor-neutral`, meaning that it can work with different types of hardware and cloud services, making it a flexible and powerful solution for managing `containerized applications`.
- In addition to Rancher, Rancher Labs has also released other open source products, such as `RancherOS`, `RKE`, `K3s`, and `Longhorn`. These products are designed to work seamlessly with Rancher and provide additional functionality for managing `containerized workloads`.
- Rancher Labs is committed to the principles of `open source software` and has made all of its products freely available for anyone to use and modify. This allows the community to contribute to the development of Rancher and its related products, making them even better over time.

# Rancher's earlier products

Rancher Labs is a company that provides open source container orchestration software, with a focus on community-driven development. Its main product, `Rancher`, is a management platform for containerized workloads on-premises and in the cloud. `Rancher` is vendor-neutral and can deploy workloads on various types of hardware. Rancher Labs also has other open source products, including `RancherOS`, `RKE`, `K3s`, and `Longhorn`.

- Rancher Labs was founded in 2014 in Cupertino, California, by Sheng Liang, Shannon Williams, Darren Shepherd, and Will Chanas.
Rancher Labs released its first product, `Rancher v1.0`, in March 2016.
- Initially, `Rancher` only supported `Docker Swarm` and `Rancher Cattle` clusters for managing containerized workloads.
`Docker Swarm` was an early cluster orchestration tool that introduced concepts such as defining an application as a group of containers that can be created and destroyed at any time, and using a virtual network to make containers accessible on all nodes in a cluster.
- Rancher Labs also developed its own Docker cluster software, called `Cattle`, which aimed to address the limitations of `Docker Swarm` in areas such as networking, load balancing, and storage.
  - Networking: `Cattle` improved upon the networking capabilities of `Docker Swarm` by allowing users to specify their own subnets for each environment, rather than being limited to a class C subnet by default. This added flexibility made it easier for users to manage their networks and avoid conflicts with existing infrastructure.
  - Load balancing: `Cattle's` use of `HAProxy` allowed for much more advanced load balancing capabilities, such as session persistence, SSL termination, and connection management. This made it easier for users to deploy complex applications that required these features.
  - Storage: `Cattle's` support for additional storage providers like `AWS` and `VMware` gave users more options for storing their data and allowed them to leverage the benefits of these platforms. `Rancher` also provided the ability to specify custom storage drivers, which gave users even more control over their storage infrastructure.
- `Cattle` introduced features such as IPsec tunnel management, `HAProxy` load balancing, and NFS storage options, and later added support for additional storage providers and external authentication providers like `Active Directory` and `LDAP`.
- Rancher Labs has released several open source products, including `Rancher`, `RancherOS`, `RKE`, `K3s`, and `Longhorn`.
Rancher Labs' flagship product is `Rancher`, which is a management and orchestration platform for containerized workloads both on-premises and in the cloud such as (`AWS`, `GCP`, `Azure`, `Digital Ocean`, `Civo`, `Linode`...).
`Rancher` is vendor-neutral and can deploy workloads using physical hardware in data centers,

# Rancher's main philosophy

- `Rancher's` core philosophy is centered on the idea of open source and community-driven development, and the company has continued to expand and improve its product offerings over time.

# The origins of Kubernetes

- Kubernetes, also abbreviated as `k8s`, is a cluster manager that was developed at Google from an internal project called Borg.
- The name Kubernetes originates from Greek and means `helmsman` or `pilot`.
- Borg was used to run Google's internal applications, which are made up of tens of thousands of `microservices` hosted on `clusters` worldwide.
- Borg provided three main benefits:
  - Abstraction of resource and failure management, allowing application designers to focus on application development.
  - High reliability and availability by design, achieved through the use of stateless applications that can be horizontally scaled across `clusters`.
  - Effective workload with minimal overhead on compute resources.

# The problem that Kubernetes is trying to solve

- Kubernetes is an `open-source` platform for managing `containerized` applications at scale.
- The problem Kubernetes solves is the difficulty of managing and scaling `containerized` applications in a `distributed` environment.
- Containers, such as `Docker`, make it easy to package an application and its dependencies together, but managing and scaling `multiple containers` across multiple machines can be challenging.


# Comparing Kubernetes to Docker Swarm and OpenShift

- Kubernetes is an open-source `container orchestration` system that can be used to automate the `deployment`, `scaling`, and `management of containerized applications`. It is considered to be the most `feature-rich` and mature of the three options and is widely used in production  environments.

- Docker Swarm is a `native` clustering and `orchestration` solution for Docker containers. It is simpler to set up and use than `Kubernetes`, but it also has fewer features. It is often used in `development` and `testing environments`, or in cases where a simpler orchestration solution is needed.
