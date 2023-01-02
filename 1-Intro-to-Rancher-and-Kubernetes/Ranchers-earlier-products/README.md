

Rancher Labs is a company that provides open source container orchestration software, with a focus on community-driven development. Its main product, Rancher, is a management platform for containerized workloads on-premises and in the cloud. Rancher is vendor-neutral and can deploy workloads on various types of hardware. Rancher Labs also has other open source products, including RancherOS, RKE, K3s, and Longhorn.

- Rancher Labs was founded in 2014 in Cupertino, California, by Sheng Liang, Shannon Williams, Darren Shepherd, and Will Chanas.
- Rancher Labs released its first product, Rancher v1.0, in March 2016.
- Initially, Rancher only supported Docker Swarm and Rancher Cattle clusters for managing containerized workloads.
- Docker Swarm was an early cluster orchestration tool that introduced concepts such as defining an application as a group of containers that can be created and destroyed at any time, and using a virtual network to make containers accessible on all nodes in a cluster.
- Rancher Labs also developed its own Docker cluster software, called Cattle, which aimed to address the limitations of Docker Swarm in areas such as networking, load balancing, and storage.
  - Networking: Cattle improved upon the networking capabilities of Docker Swarm by allowing users to specify their own subnets for each environment, rather than being limited to a class C subnet by default. This added flexibility made it easier for users to manage their networks and avoid conflicts with existing infrastructure.
  - Load balancing: Cattle's use of HAProxy allowed for much more advanced load balancing capabilities, such as session persistence, SSL termination, and connection management. This made it easier for users to deploy complex applications that required these features.
  - Storage: Cattle's support for additional storage providers like AWS and VMware gave users more options for storing their data and allowed them to leverage the benefits of these platforms. Rancher also provided the ability to specify custom storage drivers, which gave users even more control over their storage infrastructure.
- Cattle introduced features such as IPsec tunnel management, HAProxy load balancing, and NFS storage options, and later added support for additional storage providers and external authentication providers like Active Directory and LDAP.
- Rancher's core philosophy is centered on the idea of open source and community-driven development, and the company has continued to expand and improve its product offerings over time.
- Rancher Labs has released several open source products, including Rancher, RancherOS, RKE, K3s, and Longhorn.
- Rancher Labs' flagship product is Rancher, which is a management and orchestration platform for containerized workloads both on-premises and in the cloud such as (AWS, GCP, Azure, Digital Ocean, Civo, Linode...).
- Rancher is vendor-neutral and can deploy workloads using physical hardware in data centers, cloud VMs in AWS, or even Raspberry Pis in remote locations.

