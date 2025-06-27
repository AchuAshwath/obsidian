15-06-2025 11:35:16

Status :

Tags :

# 5 - The AWS Shared Responsibility Model

The Shared Responsibility Model is a security framework that defines the security obligations of AWS versus you, the customer. Understanding this model is fundamental to securing your cloud environment.

## AWS Shared Responsibility Model: The Core Concept

The model is best understood through a simple principle that AWS often repeats:

- **AWS is responsible for the security OF the cloud.**
    
    - This includes all the physical infrastructure that makes up the cloud: the hardware, the global network, and the physical security of their data centers (Regions, Availability Zones, Edge Locations).
        
    - It also includes the operation of their foundational, managed services like compute, storage, database, and networking.
        
- **You, the customer, are responsible for security IN the cloud.**
    
    - This includes your data and how you choose to configure the AWS services you use.
        
    - If you can configure it, you are responsible for securing it.
        

> "Customers are responsible for the security in the cloud; that's your data and configuration. On the AWS side, they are responsible for the security of the cloud; if it's anything physical or hardware, the operation of managed services, or Global Infrastructure, that's going to be on them."

## Types of Cloud Responsibilities (IaaS, PaaS, SaaS)

The amount of responsibility you have depends on the type of cloud service you use. As you move from IaaS to PaaS to SaaS, AWS takes on more responsibility.

- **On-Premise:** You are responsible for everything—from the physical security of the data center to the applications running on the servers.
    
- **Infrastructure as a Service (IaaS):**
    
    - **Example:** Amazon EC2.
        
    - **AWS Manages:** The physical hardware, data centers, and the virtualization layer (hypervisor).
        
    - **You Manage:** Everything above the hypervisor, including the guest operating system (OS), middleware, runtime, application code, and your data.
        
- **Platform as a Service (PaaS):**
    
    - **Example:** AWS Elastic Beanstalk.
        
    - **AWS Manages:** The hardware, virtualization, OS, and runtime environment.
        
    - **You Manage:** Your application code and your data.
        
    - Note: With some PaaS offerings like Elastic Beanstalk, you can still access the underlying infrastructure. If you modify it, you become responsible for those modifications.
        
- **Software as a Service (SaaS):**
    
    - **Example:** Amazon WorkDocs, Gmail.
        
    - **AWS Manages:** Nearly everything—the application, infrastructure, and all maintenance.
        
    - **You Manage:** The content of your data and the user access policies (i.e., who you share the data with).
        

## Shared Responsibility for Compute Services

The responsibility model becomes clearer when looking at specific compute services, moving from most customer responsibility to least.

1. **Bare Metal (EC2 Bare Metal):** You are responsible for the guest OS and the hypervisor (virtualization layer). AWS is only responsible for the physical machine.
    
2. **Virtual Machines (EC2):** You are responsible for the guest OS, libraries, and applications. AWS manages the host OS and the hypervisor.
    
3. **Containers (ECS/EKS):** You are responsible for configuring and managing your containers. AWS manages the underlying servers and container runtime (especially with Fargate).
    
4. **Functions (Lambda):** You are only responsible for your code. AWS manages everything else, including the container runtime, OS, and servers. This represents the highest degree of abstraction and the least customer responsibility.
    

## Shared Responsibility Model and Architecture

Your architectural choices directly influence your level of security responsibility.

- **Traditional / Virtual Machine Architecture:** Offers the most control but also places the most security responsibility on you. This is a familiar model for teams migrating from on-premise environments.
    
- **Microservices / Container Architecture:** A middle ground, where you manage the security of your containers and applications, while AWS manages the underlying hosts (especially with Fargate).
    
- **Serverless / Functions Architecture:** Involves the least responsibility for the customer. You focus solely on the security of your code and data, while AWS handles the security of the entire underlying stack. 



## References


