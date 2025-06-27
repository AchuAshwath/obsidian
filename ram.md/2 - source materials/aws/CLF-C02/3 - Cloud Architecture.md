15-06-2025 11:32:20

Status :

Tags :

# 3 - Cloud Architecture

## Cloud Architecture Terminologies

This section covers the foundational terms and concepts that cloud architects use to design robust and effective solutions on AWS.

### High Availability (HA)

High availability is the ability of a service to remain operational and accessible, ensuring there is no single point of failure.

- **Implementation:** In AWS, this is typically achieved by running your workload across multiple Availability Zones (AZs).
    
- **Example:** Using an Elastic Load Balancer (ELB) to distribute traffic across multiple EC2 instances in different AZs. If one server or AZ fails, the load balancer automatically reroutes traffic to the healthy instances.
    

### High Scalability

Scalability is the ability to increase your capacity to meet growing demand for traffic, memory, or computing power.

- **Vertical Scaling (Scaling Up):** Increasing the size and power of a single server (e.g., moving from a t2.micro to a t2.large instance).
    
- **Horizontal Scaling (Scaling Out):** Adding more servers of the same size to your resource pool. This is the more common and flexible approach in the cloud, as it also contributes to high availability.
    

### High Elasticity

Elasticity is the ability of the system to **automatically** scale resources up and down to precisely match demand.

- **Scale Out:** Automatically adding more servers when traffic spikes.
    
- **Scale In:** Automatically removing underutilized servers when traffic subsides.
    
- **Key Service:** In AWS, elasticity is primarily managed by **Auto Scaling Groups (ASGs)**, which can add or remove EC2 instances based on predefined rules and metrics (e.g., CPU utilization).
    

### Fault Tolerance

Fault tolerance is the ability of a service to prevent failure in the first place by having built-in redundancy.

- **Implementation:** A common pattern is using a **failover** system.
    
- **Example:** **RDS Multi-AZ**. This feature runs a duplicate standby database in a different AZ. All data is continuously synchronized. If the primary database fails, RDS automatically fails over to the standby database, which becomes the new primary.
    

### High Durability

Durability is the ability to recover from a disaster and prevent the loss of data.

- **Focus:** This concept is centered around **Disaster Recovery (DR)** and ensuring data is not lost.
    
- **Key Questions:** Do you have backups? How fast can you restore them? Are the backups tested and valid?
    
- **Example Service:** AWS offers services like **CloudEndure Disaster Recovery**, which continuously replicates entire machines to a low-cost staging area in another region for fast and reliable recovery.
    

## Business Continuity & Disaster Recovery

### Business Continuity Plan (BCP)

A BCP is a formal document that outlines how a business will continue operating during an unplanned disruption in service. This plan defines key metrics for recovery.

### Disaster Recovery (DR) Options

AWS outlines four main strategies for disaster recovery, each offering a different trade-off between cost and recovery time.

- **Backup and Restore (Coldest)**
    
    - **Description:** The simplest DR method. Data is backed up, and in the event of a disaster, the data is restored to new infrastructure.
        
    - **Recovery Time:** Slowest (hours).
        
    - **Cost:** Lowest.
        
- **Pilot Light (Warm)**
    
    - **Description:** A minimal version of the core services is kept running in the DR region. Data is replicated to this region. During a disaster, the core services are scaled up to handle the production load.
        
    - **Recovery Time:** Faster (tens of minutes).
        
    - **Cost:** Low, but more than Backup and Restore.
        
- **Warm Standby (Hotter)**
    
    - **Description:** A scaled-down but fully functional copy of the production environment is running in another region. In a disaster, it is scaled up to handle the full production load.
        
    - **Recovery Time:** Fast (minutes).
        
    - **Cost:** More expensive, as more resources are actively running.
        
- **Multi-site Active-Active (Hottest)**
    
    - **Description:** A full, scaled-up copy of the production environment is running in another region. Traffic is distributed between both regions, and if one fails, the other can handle the entire load.
        
    - **Recovery Time:** Near-instantaneous (near-zero downtime).
        
    - **Cost:** Highest, as you are effectively doubling your infrastructure costs.
        

### Recovery Time Objective (RTO)

RTO is the **maximum acceptable delay** between the interruption of service and the restoration of service. It answers the question: "How much downtime can our business tolerate?"

### Recovery Point Objective (RPO)

RPO is the **maximum acceptable amount of data loss** after an unplanned incident, measured in time. It answers the question: "How much data are we willing to lose?"

## Architectural Diagram Example

The course provides a walkthrough of a real-world architecture diagram for a learning platform.

- **Tools:** The diagram was created using **Adobe XD** and the official **AWS Architectural Icons**, which are free to download and provide guidelines on how to build clear diagrams.
    
- **Components:** The architecture demonstrated a traditional (non-serverless) application built on virtual machines, including:
    
    - **EC2 Instances** within an **Auto Scaling Group** in a **blue/green deployment** setup.
        
    - **Application Load Balancer (ALB)** distributing traffic from **Route 53**.
        
    - **Parameter Store** and **Secrets Manager** for storing configuration variables and database credentials.
        
    - **RDS** (Postgres) for the database.
        
    - **S3 Buckets** for storing user data, assets, and deployment artifacts.
        
    - A **CI/CD Pipeline** using AWS CodePipeline, CodeBuild, and CodeDeploy, triggered by commits to a GitHub repository.
        

## High Availability (HA) Follow Along

This section illustrates how high availability is implemented differently across various AWS services.

- **S3:** Highly available by default. When you upload an object to the S3 Standard storage class, AWS automatically replicates it across multiple AZs.
    
- **EC2:** **Not** highly available by default. A single EC2 instance is a single point of failure. To make it highly available, you must manually launch multiple instances across different AZs and use a load balancer to distribute traffic.
    
- **Elastic Beanstalk:** Provides an option to configure for high availability. When selected, it automatically provisions and configures an Application Load Balancer, an Auto Scaling Group, and multiple EC2 instances.
    
- **RDS:** Offers a "Multi-AZ" deployment option. When enabled, it creates and maintains a synchronous standby replica in a different AZ, handling failover automatically.


## References


