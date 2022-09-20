# Taskname: 6 Strategies for Migrating Applications to the Cloud, AWS Snow Family

[6 Strategies for Migrating Applications to the Cloud](https://aws.amazon.com/blogs/enterprise-strategy/6-strategies-for-migrating-applications-to-the-cloud/)

[AWS Snow Family](https://aws.amazon.com/snow/)

>  Date:20-sep-22
 ---
## 6 Strategies for Migrating Applications to the Cloud
## Rehosting:
* large legacy migration scenario where the organization is looking to scale its migration quickly to meet a business case, we find that the majority of applications are rehosted
* GE Oil & Gas, for instance, found that, even without implementing any cloud optimizations, it could save roughly 30 percent of its costs by rehosting.
* rehosting can be automated with tools (e.g. CloudEndure Migration, AWS VM Import/Export), although some customers prefer to do this manually as they learn how to apply their legacy systems to the new cloud platform.
* applications are easier to optimize/re-architect once they’re already running in the cloud
## Replatforming:
* you might make a few cloud (or other) optimizations in order to achieve some tangible benefit, but you aren’t otherwise changing the core architecture of the application. You may be looking to reduce the amount of time you spend managing database instances by migrating to a database-as-a-service platform like Amazon Relational Database Service (Amazon RDS), or migrating your application to a fully managed platform like Amazon Elastic Beanstalk.
## Repurchasing:
* Moving to a different product
## Refactoring / Re-architecting :
 *Re-imagining how the application is architected and developed, typically using cloud-native features.
*typically driven by a strong business need to add features, scale, or performance that would otherwise be difficult to achieve in the application’s existing environment.
## Retire:
* Once you’ve discovered everything in your environment, you might ask each functional area who owns each application. We’ve found that as much as 10% (I’ve seen 20%) of an enterprise IT portfolio is no longer useful, and can simply be turned off. These savings can boost the business case, direct your team’s scarce attention to the things that people use, and lessen the surface area you have to secure.
## Retain
* Usually this means “revisit” or do nothing (for now).
* Maybe you’re still riding out some depreciation, aren’t ready to prioritize an application that was recently upgraded, or are otherwise not inclined to migrate some applications. You should only migrate what makes sense for the business; and, as the gravity of your portfolio changes from on-premises to the cloud, you’ll probably have fewer reasons to retain.

AWS Snow Family
* Simple management and monitoring(AWS OpsHub is a complimentary graphical user interface (GUI) available)
* NFS endpoint( NFS v3 and v4.1 are supported so you can easily use Snow devices with your existing on-premises servers and file-based applications)
* On-board computing( computing resources to collect and process data at the edge. Devices run specific Amazon EC2 instances with processing and storage available to support your applications and AWS IoT Greengrass functions)
* Encryption(AWS Snow Family devices is automatically encrypted with 256-bit encryption keys that are managed by the AWS Key Management Service (KMS))
* Anti-tamper & Tamper-evident(Trusted Platform Module (TPM) that provides a hardware root of trust)
* End-to-end tracking(E-Ink shipping label for easy tracking and automatic label updates for return shipping using Amazon Simple Notification Service (SNS), text messages, and via the AWS Console.)
* Secure erasure(data migration job is complete and verified, AWS performs a software erasure of the device that follows the National Institute of Standards and Technology (NIST) guidelines for media sanitization)
## AWS Snow Family service models:
* AWS Snowcone(AWS Snowcone is the most compact and portable device)
* AWS Snowball(AWS Snowball is available as a Compute Optimized device or a Storage Optimized device)
* AWS Snowmobile(AWS Snowmobile is an Exabyte-scale data migration device used to move extremely large amounts of data to AWS)


|   	|AWS SNOWCONE|	AWS SNOWBALL EDGE STORAGE OPTIMIZED|	AWS SNOWBALL EDGE COMPUTE OPTIMIZED| AWS SNOWMOBILE|
|:-----:|:-----------------:|:-------------------:|:---------------------:|:-------------------:|
|Usable HDD Storage|	8 TB|	80 TB|	42 TB	|100 PB|
|Usable SSD Storage|	14 TB	|1 TB|	7.68 TB|	No|
|Usable vCPUs|	4 vCPUs	|40 vCPUs|	52 vCPUs|	N/A|
|Usable Memory|	4 GB|	 80 GB|	208 GB|	N/A|
|Device Size|	9in x 6in x 3in|	548 mm x 320 mm x 501 mm|	548 mm x 320 mm x 501 mm|	45 ft. shipping container|
| // |227 mm x 148.6 mm x 82.65 mm|//|//|//|
|Device Weight|	4.5 lbs. (2.1 kg)|	49.7 lbs. (22.3 kg)|	49.7 lbs. (22.3 kg)|	N/A|
|Storage Clustering|	No|	Yes, 5-10 nodes|	Yes, 5-10 nodes|	N/A|
|256-bit Encryption|	Yes|	Yes|	Yes|	Yes|
|HIPAA Compliant|	No|	Yes, eligible|	Yes, eligible|	Yes, eligible|




