# Task Name: 
[Amazon DMS](https://www.amazonaws.cn/en/dms/)

[Amazon Redshift](https://www.tutorialspoint.com/amazon_web_services/amazon_web_services_redshift.htm)

[Amazon Dynamo DB](https://www.dynamodbguide.com/what-is-dynamo-db/)

>  Date:14-sep-2022
---
## Amazon Database Migration Service:
Amazon Database Migration Service helps you migrate databases to Amazon Web Services quickly and securely. The source database remains fully operational during the migration, minimizing downtime to applications that rely on the database. The Amazon Database Migration Service can migrate your data to and from most widely used commercial and open-source databases.

The service supports homogenous migrations such as Oracle to Oracle, as well as heterogeneous migrations between different database platforms, such as Oracle to Amazon Aurora or Microsoft SQL Server to MySQL. It also allows you to stream data to Amazon Redshift, Amazon DynamoDB, and Amazon S3 from any of the supported sources, which are Amazon Aurora, PostgreSQL, MySQL, MariaDB, Oracle Database, SAP ASE, SQL Server, IBM DB2 LUW, and MongoDB, enabling consolidation and easy analysis of data in a petabyte-scale data warehouse. Amazon Database Migration Service can also be used for continuous data replication with high-availability.

The Amazon Web Services  Schema Conversion Tool makes heterogeneous database migrations predictable by automatically converting the source database schema and a majority of the database code objects, including views, stored procedures, and functions, to a format compatible with the target database. Any objects that cannot be automatically converted are clearly marked so that they can be manually converted to complete the migration. SCT can also scan your application source code for embedded SQL statements and convert them as part of a database schema conversion project. During this process, SCT performs cloud native code optimization by converting legacy Oracle and SQL Server functions to their equivalent Amazon Web Services service thus helping you modernize the applications at the same time of database migration. Once schema conversion is complete, SCT can help migrate data from a range of data warehouses to Amazon Redshift using built-in data migration agents.

### Use cases
* Homogeneous Database Migrations(source and target database engines are same)
* Heterogeneous Database Migrations(source and target database engines are different)
* Development and Test(migrate data both into and out of the cloud for development purposes)
* Database Consolidation(consolidate multiple source databases into a single target database)
* Continuous Data Replication(data replication)

## Amazon Redshift:
Amazon Redshift is a fully managed data warehouse service in the cloud. Its datasets range from 100s of gigabytes to a petabyte. The initial process to create a data warehouse is to launch a set of compute resources called nodes, which are organized into groups called cluster. After that you can process your queries.

Features of Amazon Redshift
* Supports VPC − The users can launch Redshift within VPC and control access to the cluster through the virtual networking environment.
* Encryption − Data stored in Redshift can be encrypted and configured while creating tables in Redshift.
* SSL − SSL encryption is used to encrypt connections between clients and Redshift.
* Scalable − With a few simple clicks, the number of nodes can be easily scaled in your Redshift data warehouse as per requirement. It also allows to scale over storage capacity without any loss in performance.
* Cost-effective − Amazon Redshift is a cost-effective alternative to traditional data warehousing practices. There are no up-front costs, no long-term commitments and on-demand pricing structure.

## Amazon Dynamo DB
### Tables, Items, and Attributes
Tables, items, and attributes are the core building blocks of DynamoDB.
An item is a single data record in a table. Each item in a table is uniquely identified by the stated 
primary key of the table
Attributes are pieces of data attached to a single item.
An attribute is comparable to a column in a relational database or a field in MongoDB

### Primary Key
Each item in a table is uniquely identified by a primary key. The primary key definition must be defined at the creation of the table, and the primary key must be provided when inserting a new item.
Simple primary key made up of just a partition key, and a composite primary key made up of a partition key and a sort key.
Composite primary key, you specify both a partition key and a sort key. The sort key is used to sort items with the same partition

### Secondary Indexes
local secondary index uses the same partition key as the underlying table but a different sort key.
setting an index with just a partition key for a table with a composite primary key.
global secondary index. A global secondary index can define an entirely different primary key for a table.


### Read and Write Capacity
When you use a database like MySQL, Postgres, or MongoDB, you provision a particular server to run your database. You'll need to choose your instance size -- how many CPUs do you need, how much RAM, how many GBs of storage, etc.

Not so with DynamoDB. Instead, you provision read and write capacity units. These units allow a given number of operations per second. This is a fundamentally different pricing paradigm than the instance-based world -- pricing can more closely reflect actual usage.

DynamoDB also has autoscaling of your read and write capacity units. This makes it much easier to scale your application up during peak times while saving money by scaling down when your users are asleep.
