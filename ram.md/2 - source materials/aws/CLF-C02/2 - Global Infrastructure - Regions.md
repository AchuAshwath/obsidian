25-04-2025 11:00:53

Status : #child

Tags : [[AWS - Cloud Practitioner]]

## What is Global Infrastructure?

[AWS Global Infrastructure](https://aws.amazon.com/about-aws/global-infrastructure/) is nothing but the globally distributed hardware and datacenters that are physically networked together to act as one large resource for the end customer, made up of 
1. Regions - 32
2. Availability Zones - 102
3. Direct Connection Locations - 115
4. Points of Presence - 550+ 
5. Local Zones - 35
6. Wavelength Zones - 29

### Regions

- Geographically distinct locations consisting of one or more **Availability Zones**.
- Every region is physically isolated from and independent of every other region.
- Each region generally consists of **3 Availability Zones**.
- US-EAST-1 - new features and billing information.
- Cost of AWS services vary per region.

**When choosing a region**
1. What Regulatory Compliance does this region meet?
2. What is the cost of AWS services in this region?
3. What AWS services are available in this region?
4. What is the distance or latency to my end-users?

### Regional vs Global Services

AWS scopes their AWS console on a selected Region, this will determine where the AWS Service will be launched, for GCP and Azure regions are asked while setting up a service but in AWS we set the region before.

Global Services AWS services which operate on multiple regions and the region will be fixed to `Global` 
Eg : Amazon S3, CloudFront, Route53, IAM

For Global services at the time of creation,
1. There is no concept of region  - IAM
2. A single region must be explicitly chose - S3 Bucket
3. A group of regions are chose - Cloud Front Distribution

### Availability Zones



## References


