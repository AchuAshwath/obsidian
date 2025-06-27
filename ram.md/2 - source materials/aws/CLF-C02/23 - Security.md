15-06-2025 11:56:24

Status :

Tags :

# Security

Security is "job zero" at AWS. This chapter covers the core security principles, services, and tools that AWS provides to help you protect your data and infrastructure.

## Foundational Security Concepts

### Defense-in-Depth

This is a security strategy that uses a multi-layered approach to protect resources. The idea is that if one layer of defense is compromised, another layer is already in place to thwart the attack. These layers, from outermost to innermost, are:

1. **Physical:** Securing data centers.
    
2. **Identity and Access:** Controlling who can access what.
    
3. **Perimeter:** Protecting against large-scale network attacks.
    
4. **Network:** Limiting communication between resources.
    
5. **Compute:** Securing virtual machines and ports.
    
6. **Application:** Ensuring application code is secure.
    
7. **Data:** Encrypting data to protect it.
    

### The CIA Triad

A foundational security model that describes the three core goals of information security:

- **Confidentiality:** Protecting data from unauthorized viewers (achieved through encryption).
    
- **Integrity:** Ensuring data is accurate and has not been tampered with (achieved through things like hashing and digital signatures).
    
- **Availability:** Ensuring that data and services are available when needed (achieved through high availability and DoS protection).
    

### Vulnerabilities

A vulnerability is a weakness or flaw in an application or system that an attacker can exploit to cause harm. Examples include insecure configurations, software bugs, or weak access controls.

## Cryptography and Encryption

Cryptography is the practice of secure communication. **Encryption** is the core process of scrambling data (plain text) into an unintelligible format (cipher text) using a key.

- **Symmetric Encryption (e.g., AES):** Uses the **same key** to both encrypt and decrypt data.
    
- **Asymmetric Encryption (e.g., RSA):** Uses a **key pair**: a public key to encrypt and a private key to decrypt.
    
- **Hashing (e.g., SHA-256):** A one-way function that converts an input into a fixed-size string of characters (a hash). It is deterministic (the same input always produces the same output) and is commonly used to securely store passwords.
    
    - **Salting:** Adding a random string to a password before hashing it to prevent attackers from using pre-computed "rainbow tables" to crack the hashes.
        
- **Digital Signatures:** A mathematical scheme used to verify the authenticity and integrity of a digital message. It uses a private key to "sign" the data and a public key to verify the signature.
    
- **Encryption in Transit vs. at Rest:**
    
    - **In Transit:** Securing data as it moves between locations (e.g., using TLS/SSL).
        
    - **At Rest:** Securing data while it is stored on a disk or in a database (e.g., using AES-256).
        

## Key AWS Security Services

### Identity and Access Management (Covered in detail in Chapter 16)

- **AWS IAM:** The core service for managing users, groups, roles, and permissions.
    

### Threat Detection and Protection

- **AWS Shield:** A managed **DDoS (Distributed Denial of Service)** protection service.
    
    - **Shield Standard:** Provides free, automatic protection against the most common network and transport layer (Layer 3/4) DDoS attacks for all AWS customers.
        
    - **Shield Advanced:** A paid service that offers more sophisticated protection against large-scale DDoS attacks, 24/7 access to a DDoS Response Team, and cost protection against usage spikes caused by an attack.
        
- **AWS WAF (Web Application Firewall):** A firewall that protects your web applications from common web exploits (Layer 7 attacks) like SQL injection and cross-site scripting (XSS). It integrates with Application Load Balancer and CloudFront.
    
- **Amazon GuardDuty:** A managed **threat detection service (IDS/IPS)** that continuously monitors your AWS accounts for malicious activity and unauthorized behavior. It analyzes CloudTrail logs, VPC Flow Logs, and DNS logs to identify potential threats.
    
- **Amazon Inspector:** An automated security assessment service that helps improve the security and compliance of applications deployed on EC2. It runs a security benchmark against your instances to check for vulnerabilities and deviations from best practices.
    
- **Amazon Macie:** A fully managed data security service that uses machine learning to discover, classify, and protect sensitive data (like PII) stored in Amazon S3.
    

### Encryption and Key Management

- **AWS KMS (Key Management Service):** A managed service that makes it easy to create and control encryption keys.
    
    - **Multi-tenant HSM:** Uses a FIPS 140-2 Level 2 validated Hardware Security Module (HSM).
        
    - **Envelope Encryption:** KMS uses this method, where a data key encrypts the data, and a master key (stored in KMS) encrypts the data key.
        
- **AWS CloudHSM:** Provides a **single-tenant**, dedicated Hardware Security Module (HSM) in the cloud. It's used when you need to meet strict compliance requirements (FIPS 140-2 Level 3) or have exclusive control over your HSM.
    
- **Hardware Security Module (HSM):** A physical computing device designed to securely store and manage cryptographic keys.
    

### Compliance and Auditing

- **AWS Artifact:** A self-service portal that provides on-demand access to AWS's compliance reports and security attestations (e.g., SOC reports, PCI reports). This is where you go to get proof that AWS is compliant with various global standards.
    
- **Penetration Testing (Pen Testing):** AWS allows customers to conduct authorized penetration tests on their own infrastructure, but there are rules and restrictions. You cannot test certain services, and you must submit a request for other types of simulated events.
    

### Secure Networking

- **AWS VPN (Virtual Private Network):** Establishes a secure, encrypted tunnel from your on-premise network to your AWS VPC.


## References


