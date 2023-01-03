<div align="center">

# Rancher Deep Dive
  <a href="https://github.com/Krishnamohan-Yerrabilli/Rancher-Deep-Dive">
    <img src="https://user-images.githubusercontent.com/58173938/210123030-3a390ec0-3fb6-4389-84f2-871f7feb9dc2.png" >
  </a>

</div>

Welcome to my repository documenting my learning journey! Within these resources, you will find detailed explanations and practical examples of various concepts that I have encountered on my path of growth and development. These resources have been compiled from a variety of sources such as websites, video tutorials, and books, and I have put a great deal of effort into creating and organizing them for your benefit. As I continue on my journey of learning, I will update this repository with new materials and insights. If you find this repository helpful and wish to use its contents for your own purposes, you are welcome to fork it. If you appreciate the time and effort that went into creating this repository, please consider showing your support by leaving a ⭐. Thank you for visiting, and happy learning guys!

<div id="top">
<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
  <li>
<h2 id="an-introduction-to-rancher-and-kubernetes">An introduction to Rancher and Kubernetes</h2>

<ul>
  <li><a href="#">The history of Rancher Labs as a company</a></li>
  <li>Products released by Rancher in the past</li>
  <li>Rancher's core ideology</li>
  <li>The origin of Kubernetes</li>
  <li>The issue that Kubernetes aims to address</li>
  <li>Comparing Kubernetes to Docker Swarm and OpenShift</li>
  <li>A comparison of Kubernetes and Docker Swarm</li>
  <li>A comparison of Kubernetes and OpenShift</li>
  <li>A summary</li>
</ul>

<h2 id="a-high-level-overview-of-rancher-and-kubernetes">A high-level overview of Rancher and Kubernetes</h2>

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

<h2 id="setting-up-a-single-node-rancher-instance">Setting up a single-node Rancher instance</h2>

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

<h2 id="creating-rke-and-rke2-clusters">Creating RKE and RKE2 clusters</h2>

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

<h2 id="deploying-rancher-on-a-hosted-kubernetes-cluster">Deploying Rancher on a hosted Kubernetes cluster</h2>

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

<h2 id="creating-an-rke-cluster-using-rancher">Creating an RKE cluster using Rancher</h2>

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
  <li>Preparing for nodes to join Rancher</li>
  <li>Preparing the infrastructure provider</li>
  <li>Steps for creating an RKE cluster using Rancher</li>
  <li>Deploying a cluster using node pools</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="deploying-a-hosted-cluster-with-rancher">Deploying a hosted cluster with Rancher</h2>

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

<h2 id="importing-an-externally-managed-cluster-into-rancher">Importing an externally managed cluster into Rancher</h2>

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

<h2 id="installing-a-kubernetes-cluster-with-rancher-on-aws">Installing a Kubernetes cluster with Rancher on AWS</h2>

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

<h2 id="installing-a-kubernetes-cluster-with-rancher-on-gcp">Installing a Kubernetes cluster with Rancher on GCP</h2>

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

<h2 id="installing-a-kubernetes-cluster-with-rancher-on-azure">Installing a Kubernetes cluster with Rancher on Azure</h2>

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

<h2 id="upgrading-a-kubernetes-cluster">Upgrading a Kubernetes cluster</h2>

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

<h2 id="backing-up-and-restoring-a-cluster">Backing up and restoring a cluster</h2>

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


<h2 id="scaling-a-cluster">Scaling a cluster</h2>

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

<h2 id="monitoring-a-cluster">Monitoring a cluster</h2>

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

<h2 id="logging-for-a-cluster">Logging for a cluster</h2>

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

<h2 id="networking-for-a-cluster">Networking for a cluster</h2>

<ul>
  <li>Understanding the different options for networking for a cluster</li>
  <li>Requirements and limitations</li>
  <li>Basic requirements</li>
  <li>Design limitations and considerations</li>
  <li>Rules for designing a solution</li>
  <li>Setting up networking for a cluster</li>
  <li>Ongoing maintenance tasks</li>
  <li>A summary</li>
</ul>

<h2 id="storage">Storage for a cluster</h2>
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

<h2 id="security">Security for a cluster</h2>
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

<h2 id="deploying">Deploying applications to a cluster</h2>
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

<h2 id="upgrading">Upgrading applications on a cluster</h2>
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

<h2 id="migrating">Migrating applications to a cluster</h2>
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

<h2 id="monitoring">Monitoring applications on a cluster</h2>
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

<h2 id="troubleshooting">Troubleshooting applications on a cluster</h2>
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

<h2 id="best-practices">Best practices for running applications on a cluster</h2>
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

## ❤ Show your support

Give a ⭐️ if this project helped you, Happy learning!
