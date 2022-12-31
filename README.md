<div align="center">

# Rancher Deep Dive
  <a href="https://github.com/Krishnamohan-Yerrabilli/Rancher-Deep-Dive">
    <img src="https://user-images.githubusercontent.com/58173938/210123030-3a390ec0-3fb6-4389-84f2-871f7feb9dc2.png" >
  </a>

</div>

This repository is a compilation of my notes and examples from my learning journey. It includes detailed explanations and practical examples of various concepts that I have learned from a variety of sources including websites, video tutorials, and books. I have put a lot of effort into creating and organizing this repository, and I will continue to update it with new links as I continue my learning journey. If you find this repository helpful and want to use its contents for your own purposes, you can fork it. If you appreciate the time and effort that went into creating this repository, please consider giving it a ⭐ to show your support.

## An introduction to Rancher and Kubernetes

- [The history of Rancher Labs as a company]()
- Products released by Rancher in the past
- Rancher's core ideology
- The origin of Kubernetes
- The issue that Kubernetes aims to address
- Comparing Kubernetes to Docker Swarm and OpenShift
- A comparison of Kubernetes and Docker Swarm
- A comparison of Kubernetes and OpenShift
- A summary 

## A high-level overview of Rancher and Kubernetes

- The purpose of the Rancher server
- What RKE and RKE2 are
- An explanation of RKE
- An explanation of RKE2
- What K3s is
- The role of RancherD
- The controllers running inside Rancher server pods
- The function of Cattle agents
- How Rancher manages nodes and clusters
- An overview of kube-apiserver, kubecontroller-manager, kubescheduler, etcd, and kubelet
- How the current state and desired state work together
- A summary 

## Setting up a single-node Rancher instance

- What a single-node Rancher installation is
- Requirements and limitations
- Rules for designing a solution
- Steps for installation
- Installing Docker
- Preparing SSL certificates
- Starting the Rancher server
- Migrating to an HA setup
- Backing up the current Rancher server
- Starting the transition to a new cluster
- Cleaning up/rolling back
- A summary 

## Creating RKE and RKE2 clusters

- An explanation of RKE clusters
- The history of RKE
- How RKE works
- An explanation of RKE2 clusters
- The role of RancherD
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Setting up RKE clusters
- Setting up RKE2 clusters
- Install steps for RKE
- Install steps for RKE2
- Configuring an external load balancer (HAProxy)
- TCP mode
- HTTP/HTTPS mode
- Configuring MetalLB
- Installation
- Configuration
- A summary 

## Deploying Rancher on a hosted Kubernetes cluster

- Understanding hosted Kubernetes clusters
- Requirements and limitations
- Amazon EKS
- Google's GKE
- Azure's AKS
- Rules for designing a solution
- Setting up a hosted Kubernetes cluster on Amazon EKS
- Setting up a hosted Kubernetes cluster on Google's GKE
- Setting up a hosted Kubernetes cluster on Azure's AKS
- Installing and upgrading Rancher
- Installing Rancher
- Upgrading Rancher
- The Rancher Backup Operator
- Installation
- Creating a backup
- A summary 

## Creating an RKE cluster using Rancher

- What a Rancher-managed cluster is
- The origin of Rancher-managed clusters
- How Rancher manages nodes
- How Rancher manages a cluster
- Requirements and limitations
- Rancher-created managed nodes
- Existing nodes
- Rules for designing a solution
- Setting up an RKE cluster on AWS
- Setting up an RKE cluster on GCP
- Preparing for nodes to join Rancher
- Preparing the infrastructure provider
- Steps for creating an RKE cluster using Rancher
- Deploying a cluster using node pools
- Ongoing maintenance tasks
- A summary 

## Deploying a hosted cluster with Rancher

- How Rancher can manage a hosted cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Setting up a hosted cluster on Amazon EKS with Rancher
- Setting up a hosted cluster on Google's GKE with Rancher
- Setting up a hosted cluster on Microsoft Azure Kubernetes Service (AKS) with Rancher
- Preparing the cloud provider
- Setting up a hosted cluster on Amazon EKS
- Setting up a hosted cluster on Google's GKE
- Setting up a hosted cluster on AKS
- Installation steps
- Setting up a hosted cluster on Amazon EKS with Rancher
- Setting up a hosted cluster on Google's GKE with Rancher
- Setting up a hosted cluster on AKS with Rancher
- Ongoing maintenance tasks
- A summary 

## Importing an externally managed cluster into Rancher

- What an externally managed cluster is
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Importing an externally managed cluster
- Ongoing maintenance tasks
- A summary 

## Installing a Kubernetes cluster with Rancher on AWS

- Understanding the different options for installing a cluster on AWS
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Preparing the infrastructure provider
- Installation steps
- Ongoing maintenance tasks
- A summary 

## Installing a Kubernetes cluster with Rancher on GCP

- Understanding the different options for installing a cluster on GCP
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Preparing the infrastructure provider
- Installation steps
- Ongoing maintenance tasks
- A summary 

## Installing a Kubernetes cluster with Rancher on Azure

- Understanding the different options for installing a cluster on Azure
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Preparing the infrastructure provider
- Installation steps
- Ongoing maintenance tasks
- A summary 

## Upgrading a Kubernetes cluster

- Understanding the different options for upgrading a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Preparing for the upgrade
- Performing the upgrade
- Ongoing maintenance tasks
- A summary 

## Backing up and restoring a cluster

- Understanding the different options for backing up and restoring a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Backing up a cluster
- Restoring a cluster
- Ongoing maintenance tasks
- A summary 

## Scaling a cluster

- Understanding the different options for scaling a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Scaling a cluster
- Ongoing maintenance tasks
- A summary 

## Monitoring a cluster

- Understanding the different options for monitoring a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Setting up monitoring for a cluster
- Ongoing maintenance tasks
- A summary 

## Logging for a cluster

- Understanding the different options for logging for a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Setting up logging for a cluster
- Ongoing maintenance tasks
- A summary 

## Networking for a cluster

- Understanding the different options for networking for a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Setting up networking for a cluster
- Ongoing maintenance tasks
- A summary 

## Storage for a cluster

- Understanding the different options for storage for a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Setting up storage for a cluster
- Ongoing maintenance tasks
- A summary 

## Security for a cluster

- Understanding the different options for security for a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Setting up security for a cluster
- Ongoing maintenance tasks
- A summary 

## Deploying applications to a cluster

- Understanding the different options for deploying applications to a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Deploying applications to a cluster
- Ongoing maintenance tasks
- A summary 

## Upgrading applications on a cluster

- Understanding the different options for upgrading applications on a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Upgrading applications on a cluster
- Ongoing maintenance tasks
- A summary 

## Migrating applications to a cluster

- Understanding the different options for migrating applications to a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Migrating applications to a cluster
- Ongoing maintenance tasks
- A summary 

## Monitoring applications on a cluster

- Understanding the different options for monitoring applications on a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Monitoring applications on a cluster
- Ongoing maintenance tasks
- A summary 

## Troubleshooting applications on a cluster

- Understanding the different options for troubleshooting applications on a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Troubleshooting applications on a cluster
- Ongoing maintenance tasks
- A summary 

## Best practices for running applications on a cluster

- Understanding the different options for best practices for running applications on a cluster
- Requirements and limitations
- Basic requirements
- Design limitations and considerations
- Rules for designing a solution
- Best practices for running applications on a cluster
- Ongoing maintenance #tasks
- A summary
