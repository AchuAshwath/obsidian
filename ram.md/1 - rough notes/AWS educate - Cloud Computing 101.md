27-05-2025 16:14:11

Status :

Tags :

# Module 4

### S3 - Simple Storage Service
1. search for S3
2. create bucket
	1. give bucket name - unique : eg - mybucketname123
	2. you can change the region
	3. default Object Ownership settings - ACLs disabled
	4. Block all public acess
	5. Bucket Versioning disabled
	6. create bucket button
3. now that the bucket is created, navigate to the bucket
4. There are three different ways to upload files
	1. Add Files
		1. click the upload button
		2. you can use add files options to add individual files
		3. you can choose all the files and the click the upload
		4. notice the success notification
	2. Add Folder
		1. click the upload button
		2. choose the desired folder and click the upload folder
	3. Drag and Drop
		1. click the upload button 
		2. Find the file you want to upload and drag and drop it
5. **View** a object 
	1. click on the file you want to view
	2. copy the object URL
	3. paste it in browser tab
	4. you may see *access denied*, this is due to the permission we gave during creating the bucket
6. **Update** bucket permissions
	1. Go to bucket > permissions
	2. Edit Block public access
	3. Disable - but dont do this without updating the policies
	4. confirm
7. **Add a bucket Policy**
	1. Use policy examples and policy generator to understand
	2. Create a policy and Save changes.
	3. You can now see warning saying that your bucket is publicly accessible, always check if you have a policy if you see this warning.

```json
{
	"Version" : "2021-10-14",
	"Statement": [
			{
				"Sid" : "PublicReadBGetObject",
				"Effect": "Allow",
				"Principal" : "s3:GetObject",
				"Resource" : [
					"arn.aws:s3:::mybucketname123/index.html",
					"arn.aws:s3:::mybucketname123/script.js",
					"arn.aws:s3:::mybucketname123/style.css",
				]
			}
	]
}
```

### Amazon EC2 - Elastic Compute Cloud

1. Load EC2 console, Console will show all the instances in the selected region
2. Go the Launch instance section and click on Launch instance
3. provide descriptive name for the instance, additional tags can be added
4. Under application and OS images we will use the Quick start, Amazon Linux AWS instance
5. Under the Amazon Machine Image (AMI) we will use, AMAzon Linux 2 HVM - kernal (free tier)
6. **Instance type**, this defines the cpu, storage, memory and network. If you're not sure about which instance to go with use the compare instance types
7. we will go with the t2.micro
8. Under key pair, click on create new key pair
	1. key pair is the set of credentials that we will use the prove our identity securely to the ec2 instance
	2. EC2 stores the public key in the instance and you will store the private key.
	3. you will need the private key to connect to the ec2
	4. provide a appropriate name for the key pair name
	5. let key pair type be RSA
	6. Private key file format be .pem for openSSH, or use .ppk for PuTTY
	7. click on key create key pair, the file is automatically downloaded in the browser
9. **Network Settings**
	1. first we will notice the defaults
	2. a default VPC is created for every region, is already created and ready to use with default subnet and internet gateway
	3. subnet is left as no preference because AWS will choose based on the availability zones,  we can edit this.
	4. auto assign public IP is enabled by default.
	5. we can also allow specific SSH traffic from our IP or custom IP range
	6. you can also allow HTTPS traffic and HTTP from the internet
	7. for customising these network settings we will, click on the edit button
	8. If you created your own VPC, you can choose it from the drop down
	9. once you changed the VPC, now you can change the subnet
	10. auto assign will switch to disabled, so we shall change it to enable because we will need to access the instance from the internet
	11. choose to create a new security group and give a relevant name, and provide a brief description
	12. Under the Inboud security rule, let put My IP  as source type for SSH access on port 22
	13. also create a another security group for the port 80 with type HTTP and source to be Anywhere, this is done because the example is to demonstrate a public blog server.
10.  Configure your storage with allocating root volume  
11. Take a look at the summary section and click on Launch instance
12. you can view the instance 

### Amazon Virtual Private Cloud (Amazon VPC)

1. how to create a VPC?
	1. navigate to the VPC console
	2. click on your VPCs to view all the VPC on our account
	3. you can notice there is already a default VPC present in your account
	4. Default VPC is given to easily get started with amazon web services
	5. Creating a new VPC
		1. under resources to create
		2. select VPC and more
		3. for the name tag auto generation, we can change the prefix
		4. IPV4 CIDR block is already chosen, 
		5. IPv6 CIDR block we will leave it default of no IPv6 CIDR Block
		6. Default Tenancy, with default you may share the resources with other AWS clients, if you need dedicated tenancy you may choose a tenancy method for additional cost.
		7. Availability zones is set to 2, along with the number of public subnets and private subnets
		8. we didnt create a NAT gateway in this demo
		9. We will let teh VPC endpint be S3 gateway
		10. and enable DNS hostnames and DNS resolution
		11. Finally we can review the diagram.
		12. create VPC, while our VPC is being created we can see all the resources that are being created and used by aws.
2. How to add ec2 instance to the VPC
	1. launch a new ec2 instance, with similar preferences as we did before
	2. without a key pair
	3. update network settings by choosing the VPC we created
	4. Ensure that the subnet selected is public
	5. launch instance, you can find that the ec2 is deployed in the vpc that we have created in the view all instances page

### Amazon Relational Database Service (Amazon RDS)

1. create database
	1. for this demo we will use the easy create method
	2. choosing mySQL as engine
	3. DB instance size - Free tier
	4. we can configure database identifier or name
	5. we can also set the master username - admin
	6. we can specify specific password or check the auto generate password
	7. Default settings for Easy Create
		1. Encryption is enabled
		2. VPC only service - choose default VPC
		3. we can enable option group to integrate third party utilites
		4. subnet groups will be created - which is part of a VPC
		5. automatic backups are enabled
		6. not publicly accessible
		7. port is not changed
		8. we can see the identifier
		9. DB engine version along with DB parameter group
		10. performance insights and monitoring
		11. maintenance window, auto minor version upgrade enabled - which means minors updates from mysql will be updated
		12. Delete protection - will protect the database from accidental deletion
	8. create database
	9. you can see the endpoint and the port available in the dashboard
	10. we can modify configurations

### AWS Identity and Access Management (IAM)

1. Using IAM we create role and attach policies to them
2. IAM > Users > Add Users
3. we will create a new user to give access to S3
	1. Enter User name
	2. Provide user access to AWS management console
	3. Auto generated password or custom password
	4. we can prompt the new user to create a new password while singing in.
	5. create a new user group
	6. orange cube are aws managed poicies
	7. search for amazon s3 full access, click on the policy link

```json
{
	"version" : "2021-10-17",
	"Statement"  [
		{
			"Effect" : "Allow",
			"Action" : [
				"s3:*",
				"s3-object-lambda:*"
			] 
			"Resource" : "*"
		}
	]  
}
```

> the `*` in the action says, that we can perform all the actions, the resource key also contains a `*` which says the policy grants permission to all the items in the s3

4. add the user to the group that you created. 


### AWS Lambda 

1. create function
2. use blue print
3. Getting started with lambda http
4. give function name
5. for execution role, leave it default
6. acknowledge and create function
7. lambda has created a function with the template that you gave.
8. on the function overview page click on the function URL
9. set up a trigger, a tigger can a aws service or a HTTP request
10. Dynamo DB instance was created with a access group set to have permission for the DB was added to the lambda IAM role
11. add dynamo db as the trigger source, and choose the table
12. verify the trigger is enabled in the triggers dashboard

### Amazon CloudWatch demo

1. we are going to create a billing alarm using cloud watch
2. Go to the Alarms section > Billing 
3. create alarm
4. Step 1 - **Specify metric and conditions**
	1. Metric 
		1. Currency : USD
		2. Period : 6 hours
	2. Conditions 
		1. Threshold Type : static
		2. Whenever EstimatedCharges is : greater
		3. than : `[specify value]` 
5. Step 2 - **Configure actions**
	1. Notification
		1. Alarm state trigger : In alarm
		2. Send a notification to the following SNS topic - create new topic and enter email
		3. create topic
6. Step 3 - **Add name and description**
7. Step 4 - **Preview and create**

**State** 
- *Insufficient data* - it's loading
- OK - under billing threshold
- In alarm - exceeded threshold

1. creating an alarm for an ec2 instance
2. Go to the All Alarms section  
3. create alarm
4. Step 1 - **Specify metric and conditions**
	1. Metric 
		1. Select metric : ec2 > per instance metrics > CPU Utilisation
		2. Currency : USD
		3. Period : 1 minute
	2. Conditions 
		1. Threshold Type : static
		2. Whenever EstimatedCharges is : greater
		3. than : `[specify value]` 
5. Step 2 - **Configure actions**
	1. Notification
		1. Alarm state trigger : In alarm
		2. Send a notification to the following SNS topic - create new topic and enter email
		3. create topic
6. Step 3 - **give alarm name and description**
7. Step 4 - **Preview and create**

# Module 5


## References


