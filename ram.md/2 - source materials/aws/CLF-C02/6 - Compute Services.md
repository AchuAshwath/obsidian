15-06-2025 11:37:35

Status :

Tags :

# Compute Services

This chapter explores the various compute services offered by AWS, which are the foundational building blocks for running applications and workloads. The core compute service is **Amazon EC2 (Elastic Compute Cloud)**, which provides virtual machines (VMs).

> "EC2 is also considered the backbone of AWS because the majority of AWS services are using EC2 as the underlying servers, whether it's S3, RDS, DynamoDB, or Lambda."

## VMs, Containers & Serverless

AWS provides compute services across three main paradigms: Virtual Machines, Containers, and Serverless.

### 1. Virtual Machines (VMs)

A VM is an emulation of a physical computer. In AWS, launching a VM is referred to as launching an **instance**.

- **Amazon EC2:** The primary service for launching and managing VMs. It is highly configurable, allowing you to choose the OS, CPU, memory, and storage.
    
- **Amazon LightSail:** A simplified, managed virtual server service. It's a "friendly version of EC2" designed for beginners or users who need to launch a simple server (like a WordPress site) without managing the underlying complexity of AWS.
    

### 2. Containers

Containers virtualize the operating system, allowing multiple isolated workloads to run on a single OS instance. This is ideal for microservice architectures.

- **Amazon ECS (Elastic Container Service):** AWS's proprietary container orchestration service. It supports Docker containers and manages a cluster of EC2 instances for you.
    
- **Amazon EKS (Elastic Kubernetes Service):** A fully managed service for running Kubernetes, the open-source standard for container orchestration.
    
- **Amazon ECR (Elastic Container Registry):** A repository for storing, managing, and deploying your container images (like Docker images).
    

### 3. Serverless Compute

Serverless computing abstracts away the underlying servers, allowing you to run code without provisioning or managing infrastructure.

- **AWS Lambda:** A serverless function service. You upload your code, and Lambda runs it in response to triggers. You are only billed for the compute time you consume, rounded to the nearest millisecond.
    
- **AWS Fargate:** A serverless compute engine for containers that works with both ECS and EKS. It allows you to run containers without managing the underlying EC2 instances. You pay per running container, which differs from standard ECS where you pay for the EC2 instances even if they are idle.
    

## High-Performance Compute (HPC)

HPC involves using clusters of thousands of servers with high-speed connections to solve large, complex computational problems.

- **AWS Nitro System:** The underlying platform for modern EC2 instances. It is a combination of dedicated hardware and a lightweight hypervisor that enables faster performance and enhanced security. It includes:
    
    - **Nitro Cards:** Specialized hardware for VPC, EBS, and storage.
        
    - **Nitro Security Chip:** Integrated into the motherboard to protect hardware resources.
        
    - **Nitro Hypervisor:** A lightweight hypervisor providing bare-metal-like performance.
        
- **EC2 Bare Metal Instances:** These instances give you direct access to the underlying hardware with no hypervisor, offering maximum performance and control.
    
- **AWS ParallelCluster:** An open-source cluster management tool that simplifies the deployment and management of HPC clusters on AWS.
    

## Edge & Hybrid Compute

These services extend AWS compute capabilities to the edge of the network or into on-premise data centers.

- **AWS Outposts:** A physical rack of AWS servers delivered to your data center, allowing you to run AWS services on-premise for a consistent hybrid experience.
    
- **AWS Wavelength:** Deploys AWS compute and storage services at the edge of 5G telecommunication networks for ultra-low latency applications.
    
- **VMware Cloud on AWS:** Allows you to manage on-premise virtual machines (using VMware) alongside AWS resources, facilitating hybrid cloud management.
    
- **AWS Local Zones:** Small-scale extensions of an AWS Region located in major metropolitan areas, providing low-latency compute closer to end-users.
    

## Cost & Capacity Management

These services are designed to help you optimize costs and manage the capacity of your compute resources.

- **EC2 Pricing Models (Spot, Reserved, Savings Plans):** These models offer significant discounts compared to On-Demand pricing by committing to usage or by using spare capacity. (This is covered in more detail in a dedicated chapter).
    
- **AWS Batch:** Plans, schedules, and executes batch computing workloads, often utilizing Spot Instances to save costs.
    
- **AWS Compute Optimizer:** Uses machine learning to analyze your usage history and recommend ways to reduce costs and improve performance (e.g., by right-sizing instances).
    
- **EC2 Auto Scaling Groups (ASGs):** Automatically add or remove EC2 instances to match demand, ensuring you only pay for the capacity you need.
    
- **Elastic Load Balancer (ELB):** Distributes traffic across multiple instances to improve availability and capacity management.
    
- **AWS Elastic Beanstalk:** A PaaS offering that simplifies deployment and automatically handles capacity provisioning, load balancing, and scaling.



## References


