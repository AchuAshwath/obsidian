15-06-2025 11:50:12

Status :

Tags :

# Serverless

Serverless computing is an architectural model where the cloud provider (AWS) is responsible for managing the underlying servers, infrastructure, and operating system. This allows developers to focus on writing code and building applications without worrying about infrastructure management.

## What is Serverless?

A service can be considered serverless if it exhibits most or all of the following characteristics:

- **No Server Management:** You do not need to provision or maintain any servers.
    
- **Abstracted Infrastructure:** The underlying compute, storage, and networking are handled entirely by the cloud provider.
    
- **High Availability & Scalability:** Serverless services are highly available and scale automatically with usage by default.
    
- **Pay-for-Value Billing:** You are billed based on the execution of your business tasks, not for idle resources. This often means you pay per request or per duration of a compute task.
    
- **Scales to Zero:** A key characteristic of many serverless services. When the service is not in use, you incur no costs.
    

> The course instructor offers an analogy: "Think of serverless like an energy-efficient rating. Some services are more serverless than others."

## Key Serverless Services on AWS

While many AWS services have serverless characteristics, this section highlights some of the most prominent ones that form the core of serverless architectures.

1. **AWS Lambda**
    
    - **Description:** A serverless **function** service. It's the central compute service in most serverless applications.
        
    - **How it Works:** You upload your code as a function, and Lambda executes it in response to an event or trigger (e.g., an API call, a file upload to S3, a message in an SQS queue).
        
    - **Billing:** You are charged only for the number of requests and the duration your code runs, measured in milliseconds.
        
2. **Amazon DynamoDB**
    
    - **Description:** A fully managed, serverless NoSQL key-value and document database.
        
    - **Features:** It provides single-digit millisecond latency at any scale and can scale to handle trillions of requests per day. You don't manage any servers or clusters.
        
3. **Amazon S3 (Simple Storage Service)**
    
    - **Description:** A serverless object storage service.
        
    - **Features:** It offers virtually unlimited storage capacity without the need to provision or manage file systems or disks.
        
4. **AWS Fargate**
    
    - **Description:** A serverless compute engine for **containers**.
        
    - **How it Works:** It allows you to run containers using ECS or EKS without managing the underlying EC2 instances. You define your container requirements, and Fargate launches and scales them for you.
        
5. **Amazon API Gateway**
    
    - **Description:** A fully managed service for creating, publishing, and securing APIs.
        
    - **Serverless Nature:** It acts as the serverless "front door" for your applications, often triggering Lambda functions in the backend. It scales automatically to handle API traffic.
        
6. **AWS Step Functions**
    
    - **Description:** A serverless orchestration service.
        
    - **Functionality:** It lets you coordinate multiple AWS services (especially Lambda functions) into a visual, serverless workflow or state machine.
        
7. **Amazon Aurora Serverless**
    
    - **Description:** An on-demand, auto-scaling version of the Aurora relational database.
        
    - **Features:** It automatically starts up, shuts down, and scales capacity up or down based on your application's needs. It's a great fit for intermittent or unpredictable database workloads.


## References


