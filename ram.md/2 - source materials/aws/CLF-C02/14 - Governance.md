15-06-2025 11:48:21

Status :

Tags :

# Governance

Cloud governance is the set of policies, processes, and controls that organizations use to manage and secure their cloud environments. AWS provides several services designed to help you implement strong governance across your accounts.
## Organizations & Accounts

### AWS Organizations

This is a central service that helps you govern your environment as you grow and scale your workloads on AWS.

- **Central Management:** Allows you to create new AWS accounts and centrally manage billing, access control, compliance, and security for all of them.
    
- **Hierarchy:** You can group accounts into **Organizational Units (OUs)** to create a hierarchy that reflects your business structure (e.g., OUs for Production, Development, Finance).
    
- **Root Account:** Your organization has a single management account (formerly called the master account).
    
- **Service Control Policies (SCPs):** These are a type of IAM policy that you can apply at the organization, OU, or individual account level. SCPs act as guardrails, defining the maximum permissions available to the entities in those accounts. For example, you could use an SCP to prevent any user (including the root user) in an account from launching resources in an unapproved region.
    

### AWS Control Tower

Control Tower provides the easiest way to set up and govern a new, secure, multi-account AWS environment based on best practices.

- **What it does:** It automates the setup of a baseline environment, or **Landing Zone**, that follows AWS well-architected principles.
    
- **Landing Zone:** This baseline environment includes:
    
    - **AWS Organizations:** To manage multiple accounts.
        
    - **AWS SSO:** For centralized identity and access management.
        
    - **Centralized Logging:** Using AWS CloudTrail and AWS Config, with logs stored in a dedicated, secure S3 bucket.
        
    - **Cross-account Security Auditing:** For centralized security monitoring.
        
- **Account Factory:** A feature within Control Tower that automates the provisioning of new AWS accounts. It ensures that any new account automatically conforms to your company-wide policies.
    
- **Guardrails:** Pre-packaged governance rules for security, operations, and compliance that you can apply across your organization. Control Tower is essentially the successor to the original AWS Landing Zone solution.
    

## Auditing and Compliance

### AWS Config

AWS Config is a service that enables you to assess, audit, and evaluate the configurations of your AWS resources. It's a key tool for **compliance as code**.

- **How it Works:** You create **Config Rules** that check whether your resources are configured as expected.
    
    - If a resource is not compliant (a state known as "drift"), AWS Config can notify you or even trigger an **auto-remediation** action (e.g., using a Lambda function) to correct the configuration.
        
- **Resource History:** Config maintains a detailed history of configuration changes for each resource, which is invaluable for auditing and troubleshooting.
    
- **Conformance Packs:** These are pre-built collections of Config Rules and remediation actions, often mapped to common compliance frameworks like CIS or NIST. They can be deployed as a single unit using a CloudFormation template.
    

## Organizing and Managing Resources

### Tagging

A tag is a label (a key-value pair) that you can assign to an AWS resource.

- **Purpose:** Tagging is a fundamental practice for organizing resources. Tags can be used for:
    
    - **Cost Management:** Tracking costs by project, department, or environment.
        
    - **Automation:** Triggering automated actions on resources with specific tags.
        
    - **Access Control:** Granting permissions based on tags in IAM policies.
        
    - **Resource Management:** Easily identifying and managing related resources.
        
- **Example:** A tag with the key Project and the value Phoenix.
    

### Resource Groups

Resource Groups allow you to create a logical grouping of resources that share one or more tags or are part of a CloudFormation stack.

- **Functionality:** It provides a unified dashboard to view and manage all the resources related to a specific project or application.
    
- **Integration with IAM:** You can use a Resource Group in an IAM policy to grant permissions to an entire collection of resources at once, simplifying policy management.
    

### AWS Quick Starts

Quick Starts are pre-built templates created by AWS and AWS Partners that help you deploy popular technologies on AWS.

- **What they are:** They are essentially sophisticated CloudFormation templates that automate the deployment of a complete architectural stack (e.g., compute, networking, storage).
    
- **Benefit:** They reduce hundreds of manual steps into a few simple ones, allowing you to launch a fully functional, production-ready environment in under an hour.
    

## Business-Centric Services

This category includes services that are designed to solve specific business problems rather than providing general-purpose infrastructure.

- **Examples:**
    
    - **Amazon Connect:** A virtual call center service.
        
    - **Amazon WorkSpaces:** A virtual remote desktop service.
        
    - **Amazon Chime:** A video conferencing service.
        
    - **Amazon Pinpoint:** A marketing campaign management service.
        
    - **Amazon QuickSight:** A business intelligence and data visualization service.
        
- **Relevance:** While not core infrastructure services, knowing what they are is useful as they may appear as "distractor" options in exam questions.


## References


