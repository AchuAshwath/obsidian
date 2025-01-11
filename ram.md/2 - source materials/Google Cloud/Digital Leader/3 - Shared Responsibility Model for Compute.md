30-12-2024 22:01:17

Status : #baby 

Tags : [[Digital Leader]] [[Shared Responsibility Model]]

# Compute as Comparison 
1. **Infrastructure as a Service(IaaS)** 
	1. **Bare Metal** (Compute Engine)
		1. *Customer* - responsible for Host OS configuration, Hypervisor.
		2. *Google* - responsible for physical machine.
	2. **Virtual Machine** (Compute Engine)
		1. *Customer* - responsible for guest OS, Container runtime.
		2. *Google* - responsible for hypervisor and the physical machine.
	3. **Google Kubernetes Engine - GKE** (Containers)
		1. *Customer* - responsible for configuring containers along with storage and deployment of containers.
		2. *Google* - responsible for OS, hypervisor and the Container Runtime.
2. **Platform as a Service (PaaS)**
	1. **App Engine** (Managed Platform)
		1. *Customer* - responsible for your code, config the environment, choose the deployment strategy they want and also configure other associated services.
		2. *Google* - Server, OS, Networking, Storage and Security.
3. **Software as a service (SaaS)**
	1.  **Word Processor** (Google docs)
		1. *Customer* - Contents of the document, management of files and configuration of the shared access control.
		2. *Google* -  Server, OS, Networking, Storage and Security.
4. **Function as a service (FaaS) or serverless**
	1. **Cloud Functions** (Server less)
		1. *Customer* - upload you code.
		2. *Google* - Deployment, Container runtime, Networking, Storage, Security, Physical machine (basically everything)
	2. **Cloud Run** - technically server less and containers

![[Pasted image 20241231165041.png]]
> Virtual machines can be single tenant or multi tenant, when its multi-tenant your machine is being used by multiple customers through virtual separation, but if you choose sole-tenant you are given that particular machine. 

### Alternate way (AWS and Azure)
*Zones* are collection of data centers within a region.
*Fault Domains* is a logical isolation of hardware within a data center or a collection of hardware and infrastructure that shares a single point of failure and is separate from other fault domains in the same availability domain.

![](https://d1.awsstatic.com/security-center/Shared_Responsibility_Model_V2.59d1eccec334b366627e9295b304202faf7b899b.jpg)

> Networks from customers to GCP differ in a way where, GCP is responsible for the routers and switches, where Customer while configuring virtual infrastructure and systems are responsible for running their own VPC or sub-nets like cloud networking services.

![[Pasted image 20241231170628.png]]
## References

[Shared responsibilities and shared fate on Google Cloud](https://cloud.google.com/architecture/framework/security/shared-responsibility-shared-fate)
[Google Cloud Digital Leader Certification Course 2024 - Pass the Exam!](https://youtu.be/cbcd6-m8sHg?si=aI3Iss2ri3_BgZLj)
[AWS - Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
[Azure - Shared Responsibility Model](https://learn.microsoft.com/en-us/azure/security/fundamentals/shared-responsibility)
