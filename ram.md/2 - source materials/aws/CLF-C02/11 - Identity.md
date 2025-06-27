15-06-2025 11:46:22

Status :

Tags :

# Identity

Identity is a critical component of cloud security. This chapter covers the models, services, and concepts that AWS uses to manage who can access what resources under which conditions.

## The Zero-Trust Model

The Zero-Trust model is a modern security framework built on the principle of **"trust no one, verify everything."** It shifts the primary security perimeter from the network to identity.

- **Old Model (Network-Centric):** Assumed that anything inside the corporate network was trusted. Security was focused on firewalls and VPNs.
    
- **New Model (Identity-Centric):** Assumes no user or device is trusted by default, regardless of its location. Every access request must be authenticated and authorized. This is better suited for modern environments with remote work and mobile devices.
    

### Zero-Trust on AWS

While AWS provides the building blocks for a Zero-Trust architecture, it doesn't offer a fully intelligent, out-of-the-box solution.

- **AWS Tools:** You can implement Zero-Trust principles using services like **IAM**, which allows for granular permissions and conditions (e.g., restricting access based on source IP, time of day, or MFA status). Services like **GuardDuty** and **CloudTrail** can be used to detect anomalous behavior.
    
- **Third-Party Integration:** For more advanced, real-time risk detection (e.g., based on device health), many organizations integrate third-party identity providers like **Azure Active Directory** or **Okta** with AWS using SSO.
    

## Core Identity Concepts

- **Directory Service:** A service that maps the names of network resources (like users, groups, and devices) to their network addresses. It acts as a central repository for managing and organizing these resources. A well-known example is **Microsoft Active Directory**.
    
- **Identity Provider (IdP):** A system that creates, maintains, and manages identity information and provides authentication services. Common examples include Google, Facebook, or a corporate directory like Azure AD.
    
- **Single Sign-On (SSO):** An authentication scheme that allows a user to log in once with a single set of credentials to access multiple independent systems. This is often achieved using standards like **SAML 2.0**.
    
- **LDAP (Lightweight Directory Access Protocol):** An open-standard protocol for accessing and maintaining directory information services. It enables **Same Sign-On** (note the difference from Single Sign-On), where users use the same credentials but may have to enter them multiple times.
    

## AWS IAM (Identity and Access Management)

IAM is the core service for managing access to AWS services and resources securely.

### Key IAM Components

- **Users:** An entity you create in AWS that represents a person or application that interacts with AWS.
    
- **Groups:** A collection of IAM users. You can apply permissions to a group, and all users in that group will inherit those permissions.
    
- **Roles:** An IAM identity with specific permissions that can be assumed by a trusted entity (like an EC2 instance, another AWS service, or a user from another account). Roles are the most secure way to grant permissions to resources, as they use temporary credentials.
    
- **Policies:** A JSON document that explicitly defines permissions. You attach policies to users, groups, or roles.
    

### Anatomy of an IAM Policy

An IAM policy is a JSON document composed of one or more statements. Each statement includes:

- **Effect:** Allow or Deny.
    
- **Action:** The specific API action being permitted or denied (e.g., s3:GetObject).
    
- **Resource:** The Amazon Resource Name (ARN) of the resource the action applies to.
    
- **Principal (for resource-based policies):** The user, account, or service that is allowed or denied access.
    
- **Condition:** Optional constraints that must be met for the policy to take effect (e.g., aws:MultiFactorAuthPresent: "true").
    

### Security Best Practices in IAM

- **Principle of Least Privilege (PoLP):** Granting only the minimum permissions necessary for a user or service to perform its task.
    
- **AWS Account Root User:** The most privileged user in an AWS account. It should **not** be used for daily tasks. Its use should be limited to specific actions only the root user can perform (e.g., changing account settings, closing the account). It is critical to secure the root user with a strong password and **Multi-Factor Authentication (MFA)**.
    
- **Multi-Factor Authentication (MFA):** A security control that requires a second form of authentication beyond a password. This can be a virtual MFA device (like Google Authenticator), a security key (like a YubiKey), or other hardware tokens.
    

## AWS SSO (Single Sign-On)

AWS SSO is a cloud-based service that makes it easy to centrally manage SSO access to multiple AWS accounts and business applications.

- **Functionality:** It allows you to create or connect your workforce identities and manage their access from a central location. Users get a single user portal to access all their assigned AWS accounts and applications without needing to re-enter credentials for each one.
    
- **Identity Sources:** You can use AWS SSO's built-in directory, or you can connect it to an external identity provider like Microsoft Active Directory.


## References


