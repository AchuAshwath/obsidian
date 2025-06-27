15-06-2025 11:41:53

Status :

Tags :

# Networking

This chapter covers the services and concepts that allow you to build and secure your network infrastructure on AWS, from isolated cloud environments to connections with your on-premise data centers.

## Cloud-Native Networking: The VPC

The foundation of networking in AWS is the **Amazon VPC (Virtual Private Cloud)**.

- **Definition:** A VPC is a logically isolated section of the AWS cloud where you can launch your AWS resources in a virtual network that you define. It gives you complete control over your virtual networking environment.
    
- **Subnets:** A VPC is divided into one or more **subnets**, which are logical partitions of your IP network. Each subnet resides entirely within one Availability Zone (AZ).
    
    - **Public Subnet:** A subnet that has a route to an **Internet Gateway (IGW)**. Resources in a public subnet can be directly accessible from the internet.
        
    - **Private Subnet:** A subnet that does not have a route to an Internet Gateway. Resources in a private subnet are not directly accessible from the internet.
        
- **Route Tables:** A set of rules, called routes, that are used to determine where network traffic from your subnet or gateway is directed. Each subnet in your VPC must be associated with a route table.
    

## VPC Security: Security Groups vs. NACLs

Securing your VPC involves two primary firewall services: Security Groups and Network Access Control Lists (NACLs). They operate at different levels and have distinct behaviors.

> "A security group acts as a firewall at the instance level... A NACL acts as a virtual firewall at the subnet level."

The key difference to remember is that you can create **deny rules** in NACLs, but **not** in Security Groups.

|   |   |   |
|---|---|---|
|Feature|Security Groups|Network Access Control Lists (NACLs)|
|**Level of Operation**|Instance level (acts on the EC2 instance's network interface)|Subnet level (acts on all traffic entering or leaving a subnet)|
|**Rule Types**|**Allow rules only**. You cannot create deny rules.|**Allow and deny rules**. You can explicitly block specific IP addresses.|
|**State**|**Stateful**. If you allow inbound traffic, the corresponding outbound traffic is automatically allowed, regardless of outbound rules.|**Stateless**. You must explicitly define rules for both inbound and outbound traffic. A response to an allowed inbound request will be denied unless there is a corresponding outbound rule.|
|**Rule Evaluation**|All rules are evaluated before a decision is made.|Rules are evaluated in numerical order, from lowest to highest. The first rule that matches the traffic is applied.|
|**Primary Use Case**|Controlling access to individual instances or groups of instances.|Acting as a primary line of defense for a subnet, often used to block known malicious IP addresses.|

## Content Delivery: Amazon CloudFront

Amazon CloudFront is AWS's **Content Delivery Network (CDN)** service.

- **Purpose:** It speeds up the delivery of your static and dynamic web content (e.g., images, videos, application files) to users across the globe.
    
- **How it Works:** CloudFront delivers your content through a worldwide network of data centers called **Edge Locations**. When a user requests your content, they are routed to the Edge Location that provides the lowest latency, so content is delivered with the best possible performance.
    
- **Integration:** It is often used with other AWS services, particularly S3 for hosting static content and Application Load Balancers for dynamic content.
    

## Enterprise & Hybrid Networking

These services are used to securely connect your existing on-premise networks to your AWS VPC.

- **AWS Virtual Private Network (VPN):**
    
    - **Function:** Establishes a secure and private encrypted tunnel from your on-premise network, office, or device to the AWS global network.
        
    - **Technology:** Uses the industry-standard **IPsec** protocol to secure the connection.
        
- **AWS Direct Connect:**
    
    - **Function:** A dedicated, private, high-speed fiber-optic connection between your data center and AWS.
        
    - **Use Case:** Ideal for enterprises that need a consistent, high-bandwidth connection and can handle higher costs. It bypasses the public internet entirely.
        
    - **Security Note:** Direct Connect provides a private connection but is **not inherently encrypted**. For end-to-end security, it is often used in combination with a VPN.
        
- **AWS PrivateLink:**
    
    - **Function:** Keeps traffic between your VPCs and supported AWS services (or your own services) on the AWS network, without traversing the public internet. This enhances security and simplifies network architecture.
        
    - **Implementation:** Achieved through **VPC Endpoints**.


## References


