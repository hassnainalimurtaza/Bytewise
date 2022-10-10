# [Shared Responsibility Model](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/PJoda/shared-responsibility-model)
The AWS Shared Responsibility Model

Throughout this course, you have learned about a variety of resources that you can create in the AWS Cloud. These resources include Amazon EC2 instances, Amazon S3 buckets, and Amazon RDS databases. Who is responsible for keeping these resources secure: you (the customer) or AWS?

The answer is both. The reason is that you do not treat your AWS environment as a single object. Rather, you treat the environment as a collection of parts that build upon each other. AWS is responsible for some parts of your environment and you (the customer) are responsible for other parts. This concept is known as the shared responsibility model.

The shared responsibility model divides into customer responsibilities (commonly referred to as “security in the cloud”) and AWS responsibilities (commonly referred to as “security of the cloud”).
![Shared Responsibility Model](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/O6M4BSJJQEWjOAUiSUBFsA_eba05e82263847828f72e132048f2d9c_Shared-Responsibility-1.png?expiry=1665532800000&hmac=Rt4tZQtcGvk3nPtaTdiZ13QXy046g5nVwW0Zt3iOOKc)

You can think of this model as being similar to the division of responsibilities between a homeowner and a homebuilder. The builder (AWS) is responsible for constructing your house and ensuring that it is solidly built. As the homeowner (the customer), it is your responsibility to secure everything in the house by ensuring that the doors are closed and locked. 

## Customers: Security in the Cloud
Customers are responsible for the security of everything that they create and put in the AWS Cloud.When using AWS services, you, the customer, maintain complete control over your content. You are responsible for managing security requirements for your content, including which content you choose to store on AWS, which AWS services you use, and who has access to that content. You also control how access rights are granted, managed, and revoked.

## AWS: Security of the Cloud
AWS is responsible for security of the cloud.AWS operates, manages, and controls the components at all layers of infrastructure. This includes areas such as the host operating system, the virtualization layer, and even the physical security of the data centers from which services operate. AWS is responsible for protecting the global infrastructure that runs all of the services offered in the AWS Cloud. This infrastructure includes AWS Regions, Availability Zones, and edge locations. 

AWS manages the security of the cloud, specifically the physical infrastructure that hosts your resources, which include:
* Physical security of data centers
* Hardware and software infrastructure
* Network infrastructure
* Virtualization infrastructure

# [User Permission and Access](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/m5XAd/user-permission-and-access)
## AWS Identity and Access Management (IAM)
AWS Identity and Access Management (IAM) enables you to manage access to AWS services and resources securely.   

IAM gives you the flexibility to configure access based on your company’s specific operational and security needs
* IAM users, groups, and roles
* IAM policies
* Multi-factor authentication

## AWS Account Root User
When you first create an AWS account, you begin with an identity known as the root user. 
The root user is accessed by signing in with the email address and password that you used to create your AWS account.It has complete access to all the AWS services and resources in the account.

![Root User](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Z2ERmg0SSyqhEZoNEpsq4w_45021d58436e46e59575c154fa7c93c5_Account-User.png?expiry=1665532800000&hmac=g1S9VPjAG7_qT52A0tRW0lpdDEwK6gls1AeKhza5Ipo)

## IAM users
An IAM user is an identity that you create in AWS. It represents the person or application that interacts with AWS services and resources. It consists of a name and credentials.By default, when you create a new IAM user in AWS, it has no permissions associated with it. To allow the IAM user to perform specific actions in AWS, such as launching an Amazon EC2 instance or creating an Amazon S3 bucket, you must grant the IAM user the necessary permissions.

## IAM policies
An IAM policy is a document that allows or denies permissions to AWS services and resources.  
IAM policies enable you to customize users’ levels of access to resources. For example, you can allow users to access all of the Amazon S3 buckets within your AWS account, or only a specific bucket.

## IAM Groups
An IAM group is a collection of IAM users. When you assign an IAM policy to a group, all users in the group are granted permissions specified by the policy.
Assigning IAM policies at the group level also makes it easier to adjust permissions when an employee transfers to a different job.

## IAM Roles
An IAM role is an identity that you can assume to gain temporary access to permissions.
Before an IAM user, application, or service can assume an IAM role, they must be granted permissions to switch to the role. When someone assumes an IAM role, they abandon all previous permissions that they had under a previous role and assume the permissions of the new role. 

## Multi-factor Authentication
Have you ever signed in to a website that required you to provide multiple pieces of information to verify your identity? You might have needed to provide your password and then a second form of authentication, such as a random code sent to your phone. This is an example of multi-factor authentication.
In IAM, multi-factor authentication (MFA) provides an extra layer of security for your AWS account.
* When a user signs in to an AWS website, they enter their IAM user ID and password. 
* The user is prompted for an authentication response from their AWS MFA device. This device could be a hardware security key, a hardware device, or an MFA application on a device such as a smartphone.
* When the user has been successfully authenticated, they are able to access the requested AWS services or resources.

# [AWS Organizations](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/h6zAG/aws-organizations)
## AWS Organizations
Suppose that your company has multiple AWS accounts. You can use AWS Organizations to consolidate and manage multiple AWS accounts within a central location.
When you create an organization, AWS Organizations automatically creates a root, which is the parent container for all the accounts in your organization. 
In AWS Organizations, you can centrally control permissions for the accounts in your organization by using service control policies (SCPs). SCPs enable you to place restrictions on the AWS services, resources, and individual API actions that users and roles in each account can access.

## Organizational Units
In AWS Organizations, you can group accounts into organizational units (OUs) to make it easier to manage accounts with similar business or security requirements. When you apply a policy to an OU, all the accounts in the OU automatically inherit the permissions specified in the policy.  
By organizing separate accounts into OUs, you can more easily isolate workloads or applications that have specific security requirements. For instance, if your company has accounts that can access only the AWS services that meet certain regulatory requirements, you can put these accounts into one OU. Then, you can attach a policy to the OU that blocks access to all other AWS services that do not meet the regulatory requirements.
![AWS Organizations](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pPdHoJ6ZSei3R6CemQno6A_46268fde3d21457383a1d27046f9ffc9_AWS-Org-1.png?expiry=1665532800000&hmac=W5AqaDSx_YdQMSlAjqyRkSIlepAg-Z8M6HW6ZRzruVg)

Imagine that your company has separate AWS accounts for the finance, information technology (IT), human resources (HR), and legal departments. You decide to consolidate these accounts into a single organization so that you can administer them from a central location. When you create the organization, this establishes the root.

![departments group together in OUs](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/FZWjTSD7RxuVo00g-5cbKg_5e1471a41368470e831db9a6e0cd6fd4_AWS-Org-2.png?expiry=1665532800000&hmac=isdu0zedbGd2oqg75CsFoGx0V_FhQYZPsnZRy9PJ8P0)

The finance and IT departments have requirements that do not overlap with those of any other department. You bring these accounts into your organization to take advantage of benefits such as consolidated billing, but you do not place them into any OUs.

![example ](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/6PR2ZzWHRZq0dmc1hzWagA_45f1951297a943b08e2897ed65c5d084_AWS-Org-3.png?expiry=1665532800000&hmac=NnXDmKtD0oz5ciZe9PCewgmPd3ryVR3_JDJX7iPD4lg)
The HR and legal departments need to access the same AWS services and resources, so you place them into an OU together. Placing them into an OU enables you to attach policies that apply to both the HR and legal departments’ AWS accounts.

# [Compliance](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/1Yi8K/compliance)
## AWS Artifact
Depending on your company’s industry, you may need to uphold specific standards. An audit or inspection will ensure that the company has met those standards.
AWS Artifact is a service that provides on-demand access to AWS security and compliance reports and select online agreements. AWS Artifact consists of two main sections: AWS Artifact Agreements and AWS Artifact Reports.

### AWS Artifact Agreements
Suppose that your company needs to sign an agreement with AWS regarding your use of certain types of information throughout AWS services. You can do this through AWS Artifact Agreements.
In AWS Artifact Agreements, you can review, accept, and manage agreements for an individual account and for all your accounts in AWS Organizations. Different types of agreements are offered to address the needs of customers who are subject to specific regulations, such as the Health Insurance Portability and Accountability Act (HIPAA).

### AWS Artifact Reports
Next, suppose that a member of your company’s development team is building an application and needs more information about their responsibility for complying with certain regulatory standards. You can advise them to access this information in AWS Artifact Reports. 
AWS Artifact Reports provide compliance reports from third-party auditors. These auditors have tested and verified that AWS is compliant with a variety of global, regional, and industry-specific security standards and regulations. AWS Artifact Reports remains up to date with the latest reports released. You can provide the AWS audit artifacts to your auditors or regulators as evidence of AWS security controls. 

![compliance reports](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zueK6sjERFqniurIxFRaEw_3ac2a00ac0684a3ab1b5a07bc01b15e5_Compliance-1.jpg?expiry=1665532800000&hmac=kKmV0jA_GzJFshHKFb3u3I9eIeO_tkDvruawu0mujLQ)

# [Denial-of-Service Attacks](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/Xq3jB/denial-of-service-attacks)
A denial-of-service (DoS) attack is a deliberate attempt to make a website or application unavailable to users

![Denial-of-Service Attacks](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/3ax8RiLVT0usfEYi1a9LaQ_57aaf02bbd614cbfb57ab2fd3bef69f2_Denial-1.png?expiry=1665532800000&hmac=-v52e69_8F4iLtc8ip82cCSZFNSMba1GMp5Ht_5mPoI)
For example, an attacker might flood a website or application with excessive network traffic until the targeted website or application becomes overloaded and is no longer able to respond. If the website or application becomes unavailable, this denies service to users who are trying to make legitimate requests.
## Distributed Denial-of-Service Attacks
![Distributed Denial-of-Service Attacks](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Jm-W9NB1Q1uvlvTQdbNblw_f1416f05e3ea41ba9004bfb9756fe401_Denial-2.png?expiry=1665532800000&hmac=Wy36INTDblOHknD1QcHISzHyYYTG2IwzAnjTR6FU88U)

In a distributed denial-of-service (DDoS) attack, multiple sources are used to start an attack that aims to make a website or application unavailable. This can come from a group of attackers, or even a single attacker. The single attacker can use multiple infected computers (also known as “bots”) to send excessive traffic to a website or application

## AWS Shield
AWS Shield is a service that protects applications against DDoS attacks. AWS Shield provides two levels of protection: Standard and Advanced.

## AWS Shield Standard
AWS Shield Standard automatically protects all AWS customers at no cost. It protects your AWS resources from the most common, frequently occurring types of DDoS attack.
As network traffic comes into your applications, AWS Shield Standard uses a variety of analysis techniques to detect malicious traffic in real time and automatically mitigates it.
## AWS Shield Advanced
AWS Shield Advanced is a paid service that provides detailed attack diagnostics and the ability to detect and mitigate sophisticated DDoS attacks. 
It also integrates with other services such as Amazon CloudFront, Amazon Route 53, and Elastic Load Balancing. Additionally, you can integrate AWS Shield with AWS WAF by writing custom rules to mitigate complex DDoS attacks.

# [Additional Security Services](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/uTXoH/additional-security-services)
## AWS Key Management Service (AWS KMS)
AWS Key Management Service (AWS KMS) enables you to perform encryption operations through the use of cryptographic keys. A cryptographic key is a random string of digits used for locking (encrypting) and unlocking (decrypting) data. You can use AWS KMS to create, manage, and use cryptographic keys. You can also control the use of keys across a wide range of services and in your applications.
With AWS KMS, you can choose the specific levels of access control that you need for your keys. For example, you can specify which IAM users and roles are able to manage keys. Alternatively, you can temporarily disable keys so that they are no longer in use by anyone. Your keys never leave AWS KMS, and you are always in control of them.
## AWS WAF
AWS WAF is a web application firewall that lets you monitor network requests that come into your web applications.AWS WAF works together with Amazon CloudFront and an Application Load Balancer. Recall the network access control lists that you learned about in an earlier module. AWS WAF works in a similar way to block or allow traffic. However, it does this by using a web access control list (ACL) to protect your AWS resources.
![AWS WAF](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/Qy75Zok7Ti2u-WaJOw4tVw_92e25f68d32c4c9694327550dabf8ae2_AWS-WAF.png?expiry=1665532800000&hmac=DnMXSxxjuuB9pJBqToeyUD2VBdYhj1KfV74196SqrfQ)

Suppose that your application has been receiving malicious network requests from several IP addresses. You want to prevent these requests from continuing to access your application, but you also want to ensure that legitimate users can still access it. You configure the web ACL to allow all requests except those from the IP addresses that you have specified.
When a request comes into AWS WAF, it checks against the list of rules that you have configured in the web ACL. If a request did not come from one of the blocked IP addresses, it allows access to the application.
![aws waf](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/1z1tqGm8T0y9bahpvB9MyA_6d1504ae0d4149489ff98e553d52d8bf_AWS-WAF-2.png?expiry=1665532800000&hmac=s0TB6pUUr0yWlvDlBixGkzoIdDGaUeLDgYSFWpFjV8Y)

## Amazon Inspector
Amazon Inspector helps to improve the security and compliance of applications by running automated security assessments. It checks applications for security vulnerabilities and deviations from security best practices, such as open access to Amazon EC2 instances and installations of vulnerable software versions. 
After Amazon Inspector has performed an assessment, it provides you with a list of security findings. The list prioritizes by severity level, including a detailed description of each security issue and a recommendation for how to fix it. However, AWS does not guarantee that following the provided recommendations resolves every potential security issue. Under the shared responsibility model, customers are responsible for the security of their applications, processes, and tools that run on AWS services.

## Amazon GuardDuty
Amazon GuardDuty is a service that provides intelligent threat detection for your AWS infrastructure and resources. It identifies threats by continuously monitoring the network activity and account behavior within your AWS environment.
![GuardDuty](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/qevzhyc9QRer84cnPYEXCA_52af9179e10748eaaa2f927292848fe9_Amazon-GuardDuty1.png?expiry=1665532800000&hmac=VldpMiKpANuwRTvMGUhM5STWnEqf7CdfWkwNcsKbcr4)
After you have enabled GuardDuty for your AWS account, GuardDuty begins monitoring your network and account activity. You do not have to deploy or manage any additional security software. GuardDuty then continuously analyzes data from multiple AWS sources, including VPC Flow Logs and DNS logs.
