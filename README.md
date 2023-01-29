<div align="center">

# Rancher Deep Dive
  <a href="https://github.com/Krishnamohan-Yerrabilli/Rancher-Deep-Dive">
    <img src="https://user-images.githubusercontent.com/58173938/210123030-3a390ec0-3fb6-4389-84f2-871f7feb9dc2.png" >
  </a>

</div>

Welcome to my learning journey repository! You'll find easy-to-understand explanations and examples of various concepts that I've encountered on my path to growth and development. These resources have been organized and presented to be as helpful as possible. As I continue learning, I'll be updating the repository with new materials and insights. Feel free to fork it if you find it helpful. If you appreciate the effort that went into creating these resources, please consider leaving a ⭐. Thank you for visiting, and happy learning guys!

<h1>Quick Start</h1>

```s
sudo docker run -d --restart=unless-stopped -p 80:80 -p 443:443 --privileged rancher/rancher
```

<div id="top">
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
  
## An introduction to Rancher and Kubernetes
  
 - [The history of Rancher Labs as a company](https://github.com/Krishnamohan-Yerrabilli/Rancher-Deep-Dive/tree/main/1-Intro-to-Rancher-and-Kubernetes#the-background-of-rancher-labs)<br>
 - [Products released by Rancher in the past](https://github.com/Krishnamohan-Yerrabilli/Rancher-Deep-Dive/tree/main/1-Intro-to-Rancher-and-Kubernetes#ranchers-earlier-products)<br>
 - [Rancher's core ideology](https://github.com/Krishnamohan-Yerrabilli/Rancher-Deep-Dive/tree/main/1-Intro-to-Rancher-and-Kubernetes#ranchers-main-philosophy)<br>
 - [The origin of Kubernetes](https://github.com/Krishnamohan-Yerrabilli/Rancher-Deep-Dive/tree/main/1-Intro-to-Rancher-and-Kubernetes#the-origins-of-kubernetes)<br>
 - [The issue that Kubernetes aims to address](https://github.com/Krishnamohan-Yerrabilli/Rancher-Deep-Dive/tree/main/1-Intro-to-Rancher-and-Kubernetes#the-problem-that-kubernetes-is-trying-to-solve) <br>
 - [Comparing Kubernetes to Docker Swarm and OpenShift](https://github.com/Krishnamohan-Yerrabilli/Rancher-Deep-Dive/tree/main/1-Intro-to-Rancher-and-Kubernetes#comparing-kubernetes-to-docker-swarm-and-openshift)<br>
 - A comparison of Kubernetes and Docker Swarm <br>
 - A comparison of Kubernetes and OpenShift <br>
 - A summary <br>

<h2 id="a-high-level-overview-of-rancher-and-kubernetes">2. A high-level overview of Rancher and Kubernetes</h2>

<ul>
  <li>The purpose of the Rancher server</li>
  <li>What RKE and RKE2 are</li>
  <li>An explanation of RKE</li>
  <li>An explanation of RKE2</li>
  <li>What K3s is</li>
  <li>The role of RancherD</li>
  <li>The controllers running inside Rancher server pods</li>
  <li>The function of Cattle agents</li>
  <li>How Rancher manages nodes and clusters</li>
  <li>An overview of kube-apiserver, kubecontroller-manager, kubescheduler, etcd, and kubelet</li>
  <li>How the current state and desired state work together</li>
  <li>A summary</li>
</ul>

<h2 id="setting-up-a-single-node-rancher-instance">3. Setting up a single-node Rancher instance</h2>

<ul>
  <li>What a single-node Rancher installation is</li>
  <li>Requirements and limitations</li>
  <li>Rules for designing a solution</li>
  <li>Steps for installation</li>
  <li>Installing Docker</li>
  <li>Preparing SSL certificates</li>
  <li>Starting the Rancher server</li>
  <li>Migrating to an HA setup</li>
  <li>Backing up the current Rancher server</li>
  <li>Starting the transition to a new cluster</li>
  <li>Cleaning up/rolling back</li>
  <li>A summary</li>
</ul>

<h2 id="creating-rke-and-rke2-clusters">4. Creating RKE and RKE2 clusters</h2>

<ul>
  <li>An explanation of RKE clusters</li>
  <li>The history of RKE</li>
  <li>How RKE works</li>
  <li>An explanation of RKE2 clusters</li>
  <li>The role of RancherD</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Setting up RKE clusters</li>
  <li>Setting up RKE2 clusters</li>
  <li>Install steps for RKE</li>
  <li>Install steps for RKE2</li>
  <li>Configuring an external load balancer (HAProxy)</li>
  <li>TCP mode</li>
  <li>HTTP/HTTPS mode</li>
  <li>Configuring MetalLB</li>
  <li>Installation</li>
  <li>Configuration</li>
  <li>A summary</li>
</ul>

<h2 id="deploying-rancher-on-a-hosted-kubernetes-cluster">5. Deploying Rancher on a hosted Kubernetes cluster</h2>

<ul>
  <li>Understanding hosted Kubernetes clusters</li>
  <li>Requirements and limitations</li>
  <li>Amazon EKS</li>
  <li>Google's GKE</li>
  <li>Azure's AKS</li>
  <li>Rules for designing a solution</li>
  <li>Setting up a hosted Kubernetes cluster on Amazon EKS</li>
  <li>Setting up a hosted Kubernetes cluster on Google's GKE</li>
  <li>Setting up a hosted Kubernetes cluster on Azure's AKS</li>
  <li>Installing and upgrading Rancher</li>
  <li>Installing Rancher</li>
  <li>Upgrading Rancher</li>
  <li>The Rancher Backup Operator</li>
  <li>Installation</li>
  <li>Creating a backup</li>
  <li>A summary</li>
</ul>

<h2 id="creating-an-rke-cluster-using-rancher">6. Creating an RKE cluster using Rancher</h2>

<ul>
  <li>What a Rancher-managed cluster is</li>
  <li>The origin of Rancher-managed clusters</li>
  <li>How Rancher manages nodes</li>
  <li>How Rancher manages a cluster</li>
  <li>Requirements and limitations</li>
  <li>Rancher-created managed nodes</li>
  <li>Existing nodes</li>
  <li>Rules for designing a solution</li>
  <li>Setting up an RKE cluster on AWS</li>
  <li>Setting up an RKE cluster on GCP</li>
  <li>Preparing for nodes to join Rancher(cohesive)</li>
  <li>Preparing the infrastructure provider</li>
  <li>Steps for creating an RKE cluster using Rancher</li>
  <li>Deploying a cluster using node pools</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="deploying-a-hosted-cluster-with-rancher">7. Deploying a hosted cluster with Rancher</h2>

<ul>
  <li>How Rancher can manage a hosted cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Setting up a hosted cluster on Amazon EKS with Rancher</li>
  <li>Setting up a hosted cluster on Google's GKE with Rancher</li>
  <li>Setting up a hosted cluster on Microsoft Azure Kubernetes Service (AKS) with Rancher</li>
  <li>Preparing the cloud provider</li>
  <li>Setting up a hosted cluster on Amazon EKS</li>
  <li>Setting up a hosted cluster on Google's GKE</li>
  <li>Setting up a hosted cluster on AKS</li>
  <li>Installation steps</li>
  <li>Setting up a hosted cluster on Amazon EKS with Rancher</li>
  <li>Setting up a hosted cluster on Google's GKE with Rancher</li>
  <li>Setting up a hosted cluster on AKS with Rancher</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="importing-an-externally-managed-cluster-into-rancher">8. Importing an externally managed cluster into Rancher</h2>

<ul>
  <li>What an externally managed cluster is</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Importing an externally managed cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="installing-a-kubernetes-cluster-with-rancher-on-aws">9. Installing a Kubernetes cluster with Rancher on AWS</h2>

<ul>
  <li>Understanding the different options for installing a cluster on AWS</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Preparing the infrastructure provider</li>
  <li>Installation steps</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="installing-a-kubernetes-cluster-with-rancher-on-gcp">10. Installing a Kubernetes cluster with Rancher on GCP</h2>

<ul>
  <li>Understanding the different options for installing a cluster on GCP</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Preparing the infrastructure provider</li>
  <li>Installation steps</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="installing-a-kubernetes-cluster-with-rancher-on-azure">11. Installing a Kubernetes cluster with Rancher on Azure</h2>

<ul>
  <li>Understanding the different options for installing a cluster on Azure</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Preparing the infrastructure provider</li>
  <li>Installation steps</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="upgrading-a-kubernetes-cluster">12. Upgrading a Kubernetes cluster</h2>

<ul>
  <li>Understanding the different options for upgrading a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Preparing for the upgrade</li>
  <li>Performing the upgrade</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="backing-up-and-restoring-a-cluster">13. Backing up and restoring a cluster</h2>

<ul>
  <li>Understanding the different options for backing up and restoring a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Backing up a cluster</li>
  <li>Restoring a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>


<h2 id="scaling-a-cluster">14. Scaling a cluster</h2>

<ul>
  <li>Understanding the different options for scaling a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Scaling a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="monitoring-a-cluster">15. Monitoring a cluster</h2>

<ul>
  <li>Understanding the different options for monitoring a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Setting up monitoring for a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="logging-for-a-cluster">16. Logging for a cluster</h2>

<ul>
  <li>Understanding the different options for logging for a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Setting up logging for a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="networking-for-a-cluster">17. Networking for a cluster</h2>

<ul>
  <li>Understanding the different options for networking for a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Networking setup for a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="storage">18. Storage for a cluster</h2>
<ul>
  <li>Understanding the different options for storage for a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Setting up storage for a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="security">19. Security for a cluster</h2>
<ul>
  <li>Understanding the different options for security for a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Setting up security for a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="deploying">20. Deploying applications to a cluster</h2>
<ul>
  <li>Understanding the different options for deploying applications to a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Deploying applications to a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="upgrading">21. Upgrading applications on a cluster</h2>
<ul>
  <li>Understanding the different options for upgrading applications on a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Upgrading applications on a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="migrating">22. Migrating applications to a cluster</h2>
<ul>
  <li>Understanding the different options for migrating applications to a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Migrating applications to a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="monitoring">23. Monitoring applications on a cluster</h2>
<ul>
  <li>Understanding the different options for monitoring applications on a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Monitoring applications on a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="troubleshooting">24. Troubleshooting applications on a cluster</h2>
<ul>
  <li>Understanding the different options for troubleshooting applications on a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Troubleshooting applications on a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="best-practices">25. Best practices for running applications on a cluster</h2>
<ul>
  <li>Understanding the different options for best practices for running applications on a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Best practices for running applications on a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

</div>

<h1>Installing Rancher on DigitalOcean</h1>

<h3>Step 1: Create a new Droplet on DigitalOcean</h3>
<p>Select the operating system of your choice, but make sure it is compatible with Rancher.</p>

<h3>Step 2: SSH into your Droplet</h3>

<h3>Step 3: Install Docker</h3>

```s
sudo apt-get update && sudo apt-get install docker.io
```

<h3>Step 4: Start the Docker daemon</h3>

```s
sudo systemctl start docker
```

<h3>Step 5: Verify that Docker is running</h3>

```s
sudo docker run hello-world
```

<h3>Step 6: Run the Rancher server</h3>

```s
sudo docker run -d --restart=unless-stopped -p 80:80 -p 443:443 rancher/rancher
```

<h3>Step 7: Open the Rancher login page in a web browser</h3>
<p>Go to the IP address of your Droplet. You should see the Rancher login page.</p>

<h3>Step 8: Complete the installation and set up your Rancher server</h3>
<p>Follow the prompts to complete the installation and set up your Rancher server.</p>

##   
  
<h1>Installing Rancher on Google Cloud Platform</h1>

<h3>Step 1: Create a new GCP project</h3>

<h3>Step 2: Create a new Compute Engine instance</h3>
<p>Select the operating system of your choice, but make sure it is compatible with Rancher.</p>

<h3>Step 3: SSH into your Compute Engine instance</h3>

<h3>Step 4: Install Docker</h3>
  
```s
sudo apt-get update && sudo apt-get install docker.io
```

<h3>Step 5: Start the Docker daemon</h3>

```s
  sudo systemctl start docker
```

<h3>Step 6: Verify that Docker is running</h3>

```s
sudo docker run hello-world
```

<h3>Step 7: Run the Rancher server</h3>

```s
  sudo docker run -d --restart=unless-stopped -p 80:80 -p 443:443 rancher/rancher
```

<h3>Step 8: Open the Rancher login page in a web browser</h3>
<p>Go to the IP address of your Compute Engine instance. You should see the Rancher login page.</p>

<h3>Step 9: Complete the installation and set up your Rancher server</h3>
<p>Follow the prompts to complete the installation and set up your Rancher server.</p>  
 
## ❤ Show your support

Give a ⭐️ if this project helped you, Happy learning!
