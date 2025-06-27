15-06-2025 11:39:20

Status :

Tags :

# 7 - Storage Services

# Storage Services

AWS provides a wide range of storage services, each designed for a specific use case. The three fundamental types of storage are Object, Block, and File.

## Introduction to the Three Core Storage Types

1. **Object Storage (S3 - Simple Storage Service)**
    
    - **Concept:** Data is stored as objects, which include the data itself, metadata, and a unique ID. It's designed for massive scalability with virtually no limit on the number of files or total storage.
        
    - **Analogy:** Think of it as a valet service for your files. You hand over your file (object), and AWS takes care of where and how it's stored.
        
    - **Access:** Accessed via an API (HTTPS). It is not meant to be mounted like a traditional hard drive.
        
    - **Best For:** Storing unstructured data like images, videos, backups, and static website assets. It's not suited for high-performance, low-latency I/O operations like running an operating system.
        
2. **Block Storage (EBS - Elastic Block Store)**
    
    - **Concept:** Data is split into evenly sized blocks and is directly accessed by the operating system. It mimics a traditional hard drive.
        
    - **Analogy:** It's a virtual hard drive that you "attach" to your EC2 virtual machine.
        
    - **Access:** It supports only a single-write volume, meaning it can only be attached to one EC2 instance at a time.
        
    - **Best For:** The root volume for an EC2 instance (where the OS is installed) or for any application that requires a dedicated, low-latency disk (e.g., a database running on an EC2 instance).
        
3. **File Storage (EFS - Elastic File System)**
    
    - **Concept:** A traditional file system hierarchy (folders and files) that can be accessed over a network.
        
    - **Analogy:** A shared network drive (like an NFS share) that multiple computers can connect to simultaneously.
        
    - **Access:** Supports multiple read/write connections at the same time and provides file-locking capabilities to manage concurrent access.
        
    - **Best For:** Use cases where multiple EC2 instances need to access and modify the same set of files, such as a shared content repository for a web application or a home directory for multiple users.
        

## Key Storage Services in Detail

### Amazon S3 (Simple Storage Service)

S3 is AWS's flagship object storage service, and it's one of its oldest and most popular offerings.

- **Buckets:** Objects are stored in containers called **buckets**. Bucket names must be **globally unique**, similar to a domain name.
    
- **Objects:** Objects are the files you store. They consist of a key (the name), a value (the data), and metadata. An individual object can be up to 5 TB in size.
    
- **S3 Storage Classes:** S3 offers different storage classes that trade retrieval time and availability for lower cost. This allows you to optimize costs based on how frequently you need to access your data.
    
    - **S3 Standard:** The default tier. Offers high durability, availability, and performance for frequently accessed data.
        
    - **S3 Intelligent-Tiering:** Automatically moves data to the most cost-effective access tier based on usage patterns.
        
    - **S3 Standard-Infrequent Access (Standard-IA):** For data that is accessed less frequently but requires rapid access when needed. It has a lower storage cost but a per-GB retrieval fee.
        
    - **S3 One Zone-IA:** Similar to Standard-IA but stores data in a single Availability Zone, making it cheaper but less resilient. Good for data that can be easily recreated.
        
    - **S3 Glacier Instant Retrieval, Flexible Retrieval, and Deep Archive:** These are for long-term data archiving. Retrieval times range from milliseconds (Instant) to minutes or hours (Flexible/Deep Archive), but they offer the lowest storage costs.
        

### AWS Snow Family

This is a suite of physical devices used to migrate large amounts of data into or out of the cloud, especially when network transfer is too slow or costly.

- **Snowcone:** The smallest device, holding 8 TB or 14 TB of data.
    
- **Snowball Edge:** A briefcase-sized device, offering Storage Optimized (80 TB) or Compute Optimized models. The compute models have more vCPUs and memory for edge processing.
    
- **Snowmobile:** A massive 45-foot shipping container on a truck, capable of moving up to 100 petabytes of data at once.
    

### Other Important Storage Services

- **AWS Storage Gateway:** A hybrid cloud storage service that connects your on-premise environment to AWS storage. It can present S3 as a file share, a local disk (volume), or a virtual tape library for backups.
    
- **AWS Backup:** A centralized, fully managed service to automate data backup across multiple AWS services (EC2, EBS, RDS, DynamoDB, EFS).
    
- **Amazon FSx:** A service that provides fully managed third-party file systems, primarily for:
    
    - **Windows File Server:** Provides a native SMB file system for Windows-based applications.
        
    - **Lustre:** A high-performance file system for HPC workloads.

## References


