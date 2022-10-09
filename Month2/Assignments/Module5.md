# [Instance Stores and Amazon Elastic Block Store (Amazon EBS)](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/PJ6QP/instance-stores-and-amazon-elastic-block-store-amazon-ebs)
## Instance stores
Block-level storage volumes behave like physical hard drives.
An instance store provides temporary block-level storage for an Amazon EC2 instance. An instance store is disk storage that is physically attached to the host computer for an EC2 instance, and therefore has the same lifespan as the instance. When the instance is terminated, you lose any data in the instance store.
![Instance stores](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/9akZyOW7SzGpGcjluwsxmA_8c2afb3a960d4b64bee464157c63e6db_Instance-Store-1.png?expiry=1665446400000&hmac=GEZLutpDFppRjwbXjR69ZX9YdwnislSBkpDn860cOhM)
The instance is stopped or terminated.
![The instance is terminated.](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/wWXJAd3DTdSlyQHdw_3UyQ_6ac0a2bcd3694ec69f8010077113ca55_Instance-Store-2.png?expiry=1665446400000&hmac=IUjlfIBQcYqVHiVlWpoK7TpQGIjcCgkv-I2Xs46edOw)

## Amazon Elastic Block Storage (Amazon EBS)
Amazon Elastic Block Store (Amazon EBS) is a service that provides block-level storage volumes that you can use with Amazon EC2 instances. If you stop or terminate an Amazon EC2 instance, all the data on the attached EBS volume remains available.To create an EBS volume, you define the configuration (such as volume size and type) and provision it. After you create an EBS volume, it can attach to an Amazon EC2 instance.Because EBS volumes are for data that needs to persist, it’s important to back up the data. You can take incremental backups of EBS volumes by creating Amazon EBS snapshots.
![EBS](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/nF82Y_Y8QBmfNmP2PBAZ3g_09f88d1ef8d2423d879146d698712227_EBS1.png?expiry=1665446400000&hmac=LEdqZio56EXQ-bZChtm7qy5XAs0OhWgw8o0fKFid3Fw)

## Amazon EBS Snapshots
An EBS snapshot is an incremental backup. This means that the first backup taken of a volume copies all the data. For subsequent backups, only the blocks of data that have changed since the most recent snapshot are saved. 
Incremental backups are different from full backups, in which all the data in a storage volume copies each time a backup occurs. The full backup includes data that has not changed since the most recent backup.
![Snapshots](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/XfmNRhWHSn65jUYVh9p-WQ_46db8789bf184ca8a427ddc15f647523_EBS-Snapshots.png?expiry=1665446400000&hmac=q1gpQ7TSFUiKHoBY25_X1kwhblqtCimgau6QN95GNO8)

# [Amazon Simple Storage Service (Amazon S3)](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/6iBGs/amazon-simple-storage-service-amazon-s3)
## Object Storage
In object storage, each object consists of data, metadata, and a key.
The data might be an image, video, text document, or any other type of file. Metadata contains information about what the data is, how it is used, the object size, and so on. An object’s key is its unique identifier.
![Object Storage](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pPpluPW_RMe6Zbj1v6TH5w_ecbf5ac0be9247959d528841f18d0477_S3_1.png?expiry=1665446400000&hmac=0JgnF8NtTaIKNtqMI0GVQtvjV5OqCby3klznStw4F-I)

## Amazon Simple Storage Service (Amazon S3)
Amazon Simple Storage Service (Amazon S3) is a service that provides object-level storage. Amazon S3 stores data as objects in buckets.
You can upload any type of file to Amazon S3, such as images, videos, text files, and so on. For example, you might use Amazon S3 to store backup files, media files for a website, or archived documents. Amazon S3 offers unlimited storage space. The maximum file size for an object in Amazon S3 is 5 TB.

## Amazon S3 Storage Classes
With Amazon S3, you pay only for what you use. You can choose from a range of storage classes to select a fit for your business and cost needs. When selecting an Amazon S3 storage class, consider these two factors:
* How often you plan to retrieve your data
* How available you need your data to be

## Amazon S3 Standard
* Designed for frequently accessed data
* Stores data in a minimum of three Availability Zones
* Amazon S3 Standard provides high availability for objects. This makes it a good choice for a wide range of use cases, such as websites, content distribution, and data analytics. Amazon S3 Standard has a higher cost than other storage classes intended for infrequently accessed data and archival storage.

## Amazon S3 Standard-Infrequent Access (S3 Standard-IA)
* Ideal for infrequently accessed data
* Similar to Amazon S3 Standard but has a lower storage price and higher retrieval price

## Amazon S3 One Zone-Infrequent Access (S3 One Zone-IA)
* Stores data in a single Availability Zone
* Has a lower storage price than Amazon S3 Standard-IA
* You want to save costs on storage.
* You can easily reproduce your data in the event of an Availability Zone failure.

## Amazon S3 Intelligent-Tiering
* Ideal for data with unknown or changing access patterns
* Requires a small monthly monitoring and automation fee per object

## Amazon S3 Glacier Instant Retrieval
* Works well for archived data that requires immediate access
* Can retrieve objects within a few milliseconds

## Amazon S3 Glacier Flexible Retrieval
* Low-cost storage designed for data archiving
* Able to retrieve objects within a few minutes to hours

## Amazon S3 Glacier Deep Archive
* Lowest-cost object storage class ideal for archiving
* Able to retrieve objects within 12 hours

## Amazon S3 Outposts
* Creates S3 buckets on Amazon S3 Outposts
* Makes it easier to retrieve, store, and access data on AWS Outposts

# [Amazon Elastic File System (Amazon EFS)](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/kEsOH/amazon-elastic-file-system-amazon-efs)
## File Storage
In file storage, multiple clients (such as users, applications, servers, and so on) can access data that is stored in shared file folders. In this approach, a storage server uses block storage with a local file system to organize files. Clients access data through file paths.
Compared to block storage and object storage, file storage is ideal for use cases in which a large number of services and resources need to access the same data at the same time.
Amazon Elastic File System (Amazon EFS) is a scalable file system used with AWS Cloud services and on-premises resources. As you add and remove files, Amazon EFS grows and shrinks automatically. It can scale on demand to petabytes without disrupting applications. 
## Comparing Amazon EBS and Amazon EFS
### Amazon EBS
* An Amazon EBS volume stores data in a single Availability Zone. 
* To attach an Amazon EC2 instance to an EBS volume, both the Amazon EC2 instance and the EBS volume must reside within the same Availability Zone.

### Amazon EFS
* Amazon EFS is a regional service. It stores data in and across multiple Availability Zones.   
* The duplicate storage enables you to access data concurrently from all the Availability Zones in the Region where a file system is located. Additionally, on-premises servers can access Amazon EFS using AWS Direct Connect.

# [Amazon Relational Database Service (Amazon RDS)](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/qpHzy/amazon-relational-database-service-amazon-rds)
## Relational databases
In a relational database, data is stored in a way that relates it to other pieces of data. 
An example of a relational database might be the coffee shop’s inventory management system. Each record in the database would include data for a single item, such as product name, size, price, and so on.
Relational databases use structured query language (SQL) to store and query data. 

## Amazon Relational Database Service
Amazon Relational Database Service (Amazon RDS) is a service that enables you to run relational databases in the AWS Cloud.
Amazon RDS is a managed service that automates tasks such as hardware provisioning, database setup, patching, and backups. With these capabilities, you can spend less time completing administrative tasks and more time using data to innovate your applications. You can integrate Amazon RDS with other services to fulfill your business and operational needs, such as using AWS Lambda to query your database from a serverless application.

## Amazon RDS database engines
Amazon RDS is available on six database engines, which optimize for memory, performance, or input/output (I/O). Supported database engines include:
* Amazon Aurora
* PostgreSQL
* MySQL
* MariaDB
* Oracle Database
* Microsoft SQL Server

## Amazon Aurora
Amazon Aurora is an enterprise-class relational database. It is compatible with MySQL and PostgreSQL relational databases. It is up to five times faster than standard MySQL databases and up to three times faster than standard PostgreSQL databases.
Amazon Aurora helps to reduce your database costs by reducing unnecessary input/output (I/O) operations, while ensuring that your database resources remain reliable and available. 

# [Amazon DynamoDB](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/Nl38W/amazon-dynamodb)
## Nonrelational Databases
In a nonrelational database, you create tables. A table is a place where you can store and query data.
Nonrelational databases are sometimes referred to as “NoSQL databases” because they use structures other than rows and columns to organize data. One type of structural approach for nonrelational databases is key-value pairs. With key-value pairs, data is organized into items (keys), and items have attributes (values). You can think of attributes as being different features of your data.
In a key-value database, you can add or remove attributes from items in the table at any time. Additionally, not every item in the table has to have the same attributes. 

## Amazon DynamoDB
Amazon DynamoDB is a key-value database service. It delivers single-digit millisecond performance at any scale.

### Serverless
* DynamoDB is serverless, which means that you do not have to provision, patch, or manage servers. 
* You also do not have to install, maintain, or operate software.

### Automatic Scaling
* As the size of your database shrinks or grows, DynamoDB automatically scales to adjust for changes in capacity while maintaining consistent performance. 
* This makes it a suitable choice for use cases that require high performance while scaling.

# [Amazon Redshift](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/XKUTh/amazon-redshift)
Amazon Redshift is a data warehousing service that you can use for big data analytics. It offers the ability to collect data from many sources and helps you to understand relationships and trends across your data.

# [AWS Database Migration Service (AWS DMS)](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/P3ERa/aws-database-migration-service-aws-dms)
AWS Database Migration Service (AWS DMS) enables you to migrate relational databases, nonrelational databases, and other types of data stores.
With AWS DMS, you move data between a source database and a target database. The source and target databases can be of the same type or different types. During the migration, your source database remains operational, reducing downtime for any applications that rely on the database. 

## Other use cases for AWS DMS
* Development and test database migrations(test applications against production data )
* Database consolidation(Combining several databases into a single database)
* Continuous replication(ongoing copies of your data)
