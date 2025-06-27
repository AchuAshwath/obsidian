15-06-2025 11:55:42

Status :

Tags :

# Billing and Pricing

This chapter covers the essential AWS services and concepts for managing costs, understanding your bill, and optimizing your spending.

## AWS Free Services and Free Tier

- **Free Services:** Many AWS services are free to use, but the resources they provision may incur costs. Examples include IAM, VPC, Auto Scaling, CloudFormation, and Elastic Beanstalk.
    
- **AWS Free Tier:** This allows you to use certain AWS services up to a specified monthly limit at no cost.
    
    - **12-Month Free Tier:** Applies for the first 12 months after you create your account. It covers services like EC2 (t2.micro or t3.micro), RDS, and S3 up to certain usage limits.
        
    - **Always Free:** Some services have a free tier that never expires, like AWS Lambda (1 million free requests per month) and DynamoDB.
        
- **Free Tier Usage Alerts:** You can enable email alerts in your billing preferences to notify you when you are approaching or have exceeded your Free Tier limits.
    

## AWS Support Plans

AWS offers several support plans with different levels of service and cost. Knowing the differences is crucial for the exam.

|   |   |   |   |   |
|---|---|---|---|---|
|Feature|Basic (Free)|Developer|Business|Enterprise|
|**Cost**|Free|Starts at $29/mo|Starts at $100/mo|Starts at $15,000/mo|
|**Tech Support**|None|Business hours email|24/7 email, chat, phone|24/7 email, chat, phone|
|**Response Time**|N/A|< 24 hrs (general)|< 1 hr (prod down)|**< 15 mins** (business-critical down)|
|**Trusted Advisor**|7 core checks|7 core checks|**Full checks**|**Full checks**|
|**TAM**|No|No|No|**Yes** (Technical Account Manager)|
|**Concierge**|No|No|No|**Yes** (Billing & account experts)|

- **Technical Account Manager (TAM):** A designated AWS expert who provides proactive guidance, architectural reviews, and ongoing communication to help you optimize your environment. This is a key feature of the Enterprise plan.
    

## AWS Marketplace

A curated digital catalog where you can find, buy, and deploy thousands of software listings from independent software vendors (ISVs).

- **Billing Integration:** Charges for Marketplace software are integrated into your monthly AWS bill.
    

## AWS Organizations and Consolidated Billing

- **Consolidated Billing:** A key feature of **AWS Organizations**. It allows you to receive a single, consolidated bill for multiple AWS accounts.
    
- **Volume Discounts:** By combining the usage across all accounts in your organization, you can achieve a higher usage tier for services that offer volume pricing (like S3 and data transfer), resulting in a lower overall bill.
    

## Tools for Cost Management and Governance

### AWS Trusted Advisor

An automated service that acts as your cloud expert, inspecting your AWS environment and making recommendations to help you follow best practices.

- **Five Categories:** It provides checks across five categories:
    
    1. **Cost Optimization:** (e.g., identify idle load balancers)
        
    2. **Performance:** (e.g., check for high-utilization EC2 instances)
        
    3. **Security:** (e.g., check if MFA is enabled on the root account)
        
    4. **Fault Tolerance:** (e.g., check for RDS backups)
        
    5. **Service Limits:** (e.g., check if you are approaching a VPC limit)
        

### AWS Budgets

This service allows you to set custom budgets to track your costs and usage.

- **Functionality:** You can set budgets at a monthly, quarterly, or yearly level. When your actual or forecasted spending exceeds the budgeted amount, AWS can send you an alert via email or SNS.
    
- **Budget Types:** You can create budgets for overall cost, usage, or even for reservation utilization.
    

### AWS Cost Explorer

A tool that lets you visualize, understand, and manage your AWS costs and usage over time.

- **Features:**
    
    - **Visualization:** Provides default graphs for monthly costs by service or linked account.
        
    - **Filtering:** Allows you to filter and group data by various dimensions, such as service, region, or tags.
        
    - **Forecasting:** Can provide a forecast of your likely spending for the upcoming month.
        

### Cost and Usage Reports (CUR)

The CUR provides the most comprehensive and detailed set of cost and usage data available.

- **Functionality:** It generates a detailed spreadsheet (CSV) of your usage and delivers it to an S3 bucket.
    
- **Analysis:** This raw data can be ingested into other tools for deep analysis, such as **Amazon Athena** (for querying with SQL) or **Amazon QuickSight** (for creating BI dashboards).
    

### Other Key Services and Concepts

- **Cost Allocation Tags:** Tags you apply to your resources (e.g., Project: A, Department: Finance). When you activate these tags in the billing console, they appear as columns in your Cost and Usage Report, allowing you to categorize and track costs with high granularity.
    
- **Billing Alarms:** You can create alarms in **Amazon CloudWatch** to monitor your estimated charges. If your spending exceeds a defined threshold, the alarm can trigger an SNS notification.
    
- **Service Level Agreement (SLA):** A formal commitment from AWS about the expected level of service (e.g., 99.99% uptime). If AWS fails to meet an SLA, you may be eligible to receive a service credit.
    
- **AWS Service Health Dashboard vs. Personal Health Dashboard:**
    
    - **Service Health Dashboard:** Shows the general status of all AWS services in all regions.
        
    - **Personal Health Dashboard (PHD):** Provides alerts and remediation guidance for AWS events that might affect your specific environment and resources.
        
- **AWS Abuse Team:** A dedicated team for reporting suspected malicious or abusive activity originating from AWS resources (e.g., spam, DoS attacks, malware distribution). You can contact them at abuse@amazon.com.


## References


