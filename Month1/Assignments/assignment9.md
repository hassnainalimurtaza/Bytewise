# Task Name:Amazon S3,Amazon EFS,Amazon RDS
[Amazon S3]( https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html)

[Amazon EFS]( https://docs.aws.amazon.com/efs/latest/ug/whatisefs.html)

[Amazon RDS]( https://aws.amazon.com/rds/)

>  Date: 13-sep-2022
---
## Amazon S3
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. Customers of all sizes and industries can use Amazon S3 to store and protect any amount of data for a range of use cases, such as data lakes, websites, mobile applications, backup and restore, archive, enterprise applications, IoT devices, and big data analytics. Amazon S3 provides management features so that you can optimize, organize, and configure access to your data to meet your specific business, organizational, and compliance requirements.
* Storage classes
* Storage management
* Access management
* Data processing
* Storage logging and monitoring
* Analytics and insights
* Strong consistency

## How Amazon S3 works
Amazon S3 is an object storage service that stores data as objects within buckets. An object is a file and any metadata that describes the file. A bucket is a container for objects.
To store your data in Amazon S3, you first create a bucket and specify a bucket name and AWS Region. Then, you upload your data to that bucket as objects in Amazon S3. Each object has a key (or key name), which is the unique identifier for the object within the bucket.
S3 provides features that you can configure to support your specific use case. For example, you can use S3 Versioning to keep multiple versions of an object in the same bucket, which allows you to restore objects that are accidentally deleted or overwritten.
Buckets and the objects in them are private and can be accessed only if you explicitly grant access permissions. You can use bucket policies, AWS Identity and Access Management (IAM) policies, access control lists (ACLs), and S3 Access Points to manage access.

* Buckets(bucket is a container for objects)
* Objects(fundamental entities stored in Amazon S3)
* Keys(object key/key name is the unique identifier for an object within a bucket)
* S3 Versioning(keep multiple variants of an object in the same bucket)
* Version ID(unique version ID for each object)
* Bucket policy(grant access permissions to your bucket)
* S3 Access Points(named network endpoints with dedicated access policies)
* Access control lists (ACLs to grant read and write permissions)
* Regions(geographical AWS Region)

## Amazon S3 data consistency model
Amazon S3 provides strong read-after-write consistency for PUT and DELETE requests of objects in your Amazon S3 bucket in all AWS Regions. This behavior applies to both writes to new objects as well as PUT requests that overwrite existing objects and DELETE requests. In addition, read operations on Amazon S3 Select, Amazon S3 access controls lists (ACLs), Amazon S3 Object Tags, and object metadata (for example, the HEAD object) are strongly consistent.
Updates to a single key are atomic. For example, if you make a PUT request to an existing key from one thread and perform a GET request on the same key from a second thread concurrently, you will get either the old data or the new data, but never partial or corrupt data.

## Amazon Elastic File System
Amazon Elastic File System (Amazon EFS) provides a simple, serverless, set-and-forget elastic file system for use with AWS Cloud services and on-premises resources. It is built to scale on demand to petabytes without disrupting applications, growing and shrinking automatically as you add and remove files, eliminating the need to provision and manage capacity to accommodate growth. Amazon EFS has a simple web services interface that allows you to create and configure file systems quickly and easily. The service manages all the file storage infrastructure for you, meaning that you can avoid the complexity of deploying, patching, and maintaining complex file system configurations.
* Standard storage classes(EFS Standard and EFS Standard–Infrequent Access (Standard–IA), which offer multi-AZ resilience and the highest levels of durability and availability)
* One Zone storage classes(EFS One Zone and EFS One Zone–Infrequent Access (EFS One Zone–IA), which offer customers the choice of additional savings by choosing to save their data in a single Availability Zone)

You can choose from two performance modes and two throughput modes:
* _General Purpose performance mode_(web serving environments, content management systems, home directories, and general file serving)
* _Max I/O mode_( higher levels of aggregate throughput and operations per second with a tradeoff of higher latencies for file system operations)
* _Bursting_(scales as your file system grows)
* _Provisioned_(independent of the amount of data stored)

The service is designed to be highly scalable, highly available, and highly durable. Amazon EFS file systems using Standard storage classes store data and metadata across multiple Availability Zones in an AWS Region. EFS file systems can grow to petabyte scale, drive high levels of throughput, and allow massively parallel access from compute instances to your data.

## Amazon RDS
Amazon RDS is a managed relational database service that provides you six familiar database engines to choose from, including Amazon Aurora, MySQL, MariaDB, PostgreSQL, Oracle, and Microsoft SQL Server. This means that the code, applications, and tools you already use today with your existing databases can be used with Amazon RDS. Amazon RDS handles routine database tasks, such as provisioning, patching, backup, recovery, failure detection, and repair.
Amazon RDS makes it easy to use replication to enhance availability and reliability for production workloads. Using the Multi-AZ deployment option, you can run mission-critical workloads with high availability and built-in automated failover from your primary database to a synchronously replicated secondary database. Using Read Replicas, you can scale out beyond the capacity of a single database deployment for read-heavy database workloads.
As with all Amazon Web Services, there are no up-front investments required and you pay only for the resources you use.
* Lower administrative burden
* Performance
* Scalability
* Availability and durability
* Security
* Manageability
* Cost-effectiveness
