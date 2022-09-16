# Task name: Amazon Shared Responsibility Model,Denial Of Service Attacks and Protection in Amazon,Amazon KMS, WAF, Guard Duty

[Amazon Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)
 
[Denial Of Service Attacks and Protection in Amazon](https://aws.amazon.com/shield/ddos-attack-protection/)

[Amazon KMS]( https://aws.amazon.com/kms/)
[Amazon WAF](https://aws.amazon.com/waf/)
[Amazon Guard Duty](https://aws.amazon.com/blogs/security/how-to-use-amazon-guardduty-and-aws-web-application-firewall-to-automatically-block-suspicious-hosts/)

> Date: 15-sep-22
---
## Shared Responsibility Model
Security and Compliance is a shared responsibility between AWS and the customer.This shared model can help relieve the customer’s operational burden as AWS operates, manages and controls the components from the host operating system and virtualization layer down to the physical security of the facilities in which the service operates. The customer assumes responsibility and management of the guest operating system (including updates and security patches), other associated application software as well as the configuration of the AWS provided security group firewall. Customers should carefully consider the services they choose as their responsibilities vary depending on the services used, the integration of those services into their IT environment, and applicable laws and regulations. The nature of this shared responsibility also provides the flexibility and customer control that permits the deployment. As shown in the chart below, this differentiation of responsibility is commonly referred to as Security “of” the Cloud versus Security “in” the Cloud.

## AWS responsibility “Security of the Cloud” - AWS is responsible for protecting the infrastructure that runs all of the services offered in the AWS Cloud. This infrastructure is composed of the hardware, software, networking, and facilities that run AWS Cloud services.

## Customer responsibility “Security in the Cloud” – Customer responsibility will be determined by the AWS Cloud services that a customer selects. This determines the amount of configuration work the customer must perform as part of their security responsibilities.

## Applying the AWS Shared Responsibility Model in Practice
Once a customer understands the AWS Shared Responsibility Model and how it generally applies to operating in the cloud, they must determine how it applies to their use case. Customer responsibility varies based on many factors, including the AWS services and Regions they choose, the integration of those services into their IT environment, and the laws and regulations applicable to their organization and workload.

## Distributed Denial of Service (DDoS) protection service:
### WHAT IS A DDOS ATTACK?
A Denial of Service (DoS) attack is a malicious attempt to affect the availability of a targeted system, such as a website or application, to legitimate end users. Typically, attackers generate large volumes of packets or requests ultimately overwhelming the target system. In case of a Distributed Denial of Service (DDoS) attack, and the attacker uses multiple compromised or controlled sources to generate the attack.

In general, DDoS attacks can be segregated by which layer of the Open Systems Interconnection (OSI) model they attack. They are most common at the Network (layer 3), Transport (Layer 4), Presentation (Layer 6) and Application (Layer 7) Layers.

### Open Systems Interconnection (OSI) Model:

|#	|Layer|	Application|	Description|	Vector Example|
|---|---------------|-----------|-----------------|------------------|
|7|	Application|	Data|	Network process to application|	HTTP floods, DNS query floods|
|6|	Presentation|	Data|	Data representation and encryption|	SSL abuse|
|5|	Session|	Data|	Interhost communication|	N/A|
|4|	Transport|	Segments|	End-to-end connections and reliability|	SYN floods|
|3|	Network|	Packets|	Path determination and logical addressing|	UDP reflection attacks|
|2|	Datalinks|	Frames|	Physical addressing|	N/A|
|1|	Physical|	Bits|	Media, signal, and binary transmission|	N/A|


## DDOS Attack Classification
* Infrastructure Layer Attacks(Attacks at Layer 3 and 4, are typically categorized as Infrastructure layer attacks)
* Application Layer Attacks(Attacks at Layer 6 and 7, are often categorized as Application layer attacks)

## DDoS Protection Techniques
* Reduce Attack Surface Area
* Plan for Scale
* Know what is normal and abnormal traffic
* Deploy Firewalls for Sophisticated Application attacks

AWS Key Management Service (AWS KMS)
## AWS Key Management Service (AWS KMS)
![AWS KMS](https://d1.awsstatic.com/Security/aws-kms/Group%2017aws-kms.6dc3dbbbe5b75b46c4f62218d0531e5bed7276ce.png)

## AWS WAF - Web Application Firewall
AWS WAF is a web application firewall that helps protect your web applications or APIs against common web exploits and bots that may affect availability, compromise security, or consume excessive resources. AWS WAF gives you control over how traffic reaches your applications by enabling you to create security rules that control bot traffic and block common attack patterns, such as SQL injection or cross-site scripting. You can also customize rules that filter out specific traffic patterns. You can get started quickly using Managed Rules for AWS WAF, a pre-configured set of rules managed by AWS or AWS Marketplace Sellers to address issues like the OWASP Top 10 security risks and automated bots that consume excess resources, skew metrics, or can cause downtime. These rules are regularly updated as new issues emerge. AWS WAF includes a full-featured API that you can use to automate the creation, deployment, and maintenance of security rules.

![AWS WAF](https://d1.awsstatic.com/products/WAF/product-page-diagram_APIv2-AWS-WAF_How-it-Works-2x.1cafa052deabb5ca8500ce9565209f0f97725482.png)

You can deploy AWS WAF on Amazon CloudFront as part of your CDN solution, the Application Load Balancer that fronts your web servers or origin servers running on EC2, Amazon API Gateway for your REST APIs, or AWS AppSync for your GraphQL APIs. With AWS WAF, you pay only for what you use and the pricing is based on how many rules you deploy and how many web requests your application receives.
### Benefits
* Agile protection against web attacks
* Save time with managed rules
* Improved web traffic visibility
* Ease of deployment & maintenance
* Easily monitor, block, or rate-limit bots
* Security integrated with how you develop applications

 ## Amazon GuardDuty
![Amazon GuardDuty](https://d2908q01vomqb2.cloudfront.net/22d200f8670dbdb3e253a90eee5098477c95c23d/2018/07/31/GuardDuty-WAF-01.png)
