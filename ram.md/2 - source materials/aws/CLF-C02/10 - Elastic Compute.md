15-06-2025 11:43:23

Status :

Tags :

# Amazon EC2 (Elastic Compute Cloud)

This chapter provides a deeper dive into Amazon EC2, AWS's foundational service for virtual servers. EC2 is highly configurable, allowing you to tailor your compute resources to your specific needs.

## EC2 Instance Families & Types

AWS organizes EC2 instances into families, which are optimized for different use cases. Within each family, there are different instance types (sizes) that offer varying amounts of CPU, memory, and storage.

### Instance Families

AWS groups instance families into five main categories:

1. **General Purpose (e.g., T-family, M-family):**
    
    - **Description:** Provides a balance of compute, memory, and networking resources.
        
    - **Use Case:** Ideal for a wide variety of workloads, such as web servers, code repositories, and small to medium databases. This is the most common starting point.
        
2. **Compute Optimized (e.g., C-family):**
    
    - **Description:** Offers high-performance processors, making it ideal for compute-bound applications.
        
    - **Use Case:** Scientific modeling, high-performance computing (HPC), dedicated gaming servers, and ad serving engines.
        
3. **Memory Optimized (e.g., R-family, X-family):**
    
    - **Description:** Designed for workloads that process large datasets in memory.
        
    - **Use Case:** High-performance databases, in-memory caches (like Redis or Memcached), and real-time big data analytics.
        
4. **Storage Optimized (e.g., I-family, D-family):**
    
    - **Description:** Provides high, sequential read/write access to very large datasets on local storage.
        
    - **Use Case:** NoSQL databases (like Cassandra), data warehousing, and distributed file systems.
        
5. **Accelerated Computing (e.g., P-family, G-family, F-family):**
    
    - **Description:** Uses hardware accelerators, or co-processors, such as Graphics Processing Units (GPUs) or Field Programmable Gate Arrays (FPGAs).
        
    - **Use Case:** Machine learning, computational finance, seismic analysis, and graphics-intensive applications.
        

### Instance Types (Sizes)

Within each family, sizes typically double in resources and cost. Common sizes include .nano, .micro, .small, .medium, .large, .xlarge, .2xlarge, and so on.

## EC2 Tenancy

Tenancy defines how your EC2 instances are hosted on the underlying physical hardware.

1. **Shared Tenancy (Default):**
    
    - **Description:** Your EC2 instance runs on the same physical hardware as instances from other AWS customers. This is a multi-tenant model.
        
    - **Benefit:** Most cost-effective and flexible.
        
2. **Dedicated Instances:**
    
    - **Description:** Your EC2 instances run on hardware that is dedicated to your AWS account. Other customers' instances will not be on the same physical server.
        
    - **Benefit:** Meets compliance requirements that may not allow for multi-tenancy. Billed on a per-instance basis.
        
3. **Dedicated Hosts:**
    
    - **Description:** Provides you with a physical server that is fully dedicated to your use. This is a single-tenant model.
        
    - **Benefit:** Gives you the most control and visibility into the underlying hardware (e.g., sockets, cores), which is often necessary for **Bring Your Own License (BYOL)** scenarios (e.g., for certain Microsoft or Oracle licenses). Billed on a per-host basis, making it the most expensive option.
        

## Key EC2 Components & Follow Along

This section walks through launching and managing a complete, scalable web application using EC2 and related services.

### Launching an EC2 Instance

The process involves several key steps:

1. **Choose an AMI (Amazon Machine Image):** A template for the instance, containing the operating system and pre-installed software. The demo uses **Amazon Linux 2**.
    
2. **Choose an Instance Type:** The demo uses **t2.micro**, which is eligible for the Free Tier.
    
3. **Configure Instance Details:**
    
    - **User Data:** A script that runs once when the instance first launches. The demo uses a script to install and start an Apache web server (httpd).
        
    - **IAM Role:** Assigning an IAM Role to an EC2 instance grants it permissions to access other AWS services without needing to store credentials on the instance. The demo attaches a role with SSM permissions.
        
4. **Add Storage:** Configure the root volume (EBS), with options to change size and turn on encryption.
    
5. **Configure Security Group:** A virtual firewall that controls inbound and outbound traffic. The demo opens port 80 (HTTP) to allow web traffic and port 22 (SSH) for remote access.
    
6. **Launch with a Key Pair:** A key pair is required for SSH access. The demo creates a key pair to illustrate its use.
    

### Connecting to an EC2 Instance

- **SSH (Secure Shell):** The traditional method for connecting to a Linux instance. It requires the private key from your key pair.
    
- **EC2 Instance Connect & Session Manager:** AWS-native ways to connect. **Session Manager** is the preferred, more secure method as it doesn't require open inbound ports (like port 22) or SSH keys. It uses the IAM role attached to the instance for access control.
    

### Auto Scaling Group (ASG)

An ASG automatically adjusts the number of EC2 instances in a group to meet demand.

- **Configuration:** You define a **Launch Template**, a desired capacity (e.g., always keep 1 instance running), and minimum/maximum sizes.
    
- **Scaling Policies:** You can configure the ASG to scale out (add instances) or scale in (remove instances) based on metrics like CPU utilization.
    
- **Health Checks:** The ASG monitors the health of its instances and will automatically terminate and replace any that become unhealthy.
    

### Application Load Balancer (ALB)

An ALB distributes incoming application traffic across multiple targets, such as EC2 instances.

- **Function:** It increases the availability and fault tolerance of your application.
    
- **Target Groups:** An ALB forwards traffic to a **Target Group**, which contains the registered instances. The Target Group performs health checks on the instances to ensure traffic is only sent to healthy ones.
    
- **Integration with ASG:** When you connect an ALB to an ASG, the ASG automatically registers its new instances with the ALB's target group.
    

### EC2 Cleanup

The demo concludes with instructions on how to tear down the created resources to avoid incurring costs:

1. **Delete the Auto Scaling Group:** This will also terminate the EC2 instances it manages.
    
2. **Delete the Application Load Balancer.**
    
3. **Delete the Launch Template.**
    
4. **Deregister the AMI.**
    
5. **Delete the Security Group and Key Pair.**

## References


