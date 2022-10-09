# [Amazon Elastic Compute Cloud (Amazon EC2)](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/qH9Hf/amazon-elastic-compute-cloud-amazon-ec2)
Amazon Elastic Compute Cloud (Amazon EC2) provides secure, resizable compute capacity in the cloud as Amazon EC2 instances

Imagine you are responsible for the architecture of your company's resources and need to support new websites. With traditional on-premises resources, you have to do the following:
* Spend money upfront to purchase hardware.
* Wait for the servers to be delivered to you.
* Install the servers in your physical data center.
* Make all the necessary configurations.

By comparison, with an Amazon EC2 instance you can use a virtual server to run applications in the AWS Cloud.
* You can provision and launch an Amazon EC2 instance within minutes.
* You can stop using it when you have finished running a workload.
* You pay only for the compute time you use when an instance is running, not when it is stopped or terminated.
* You can save costs by paying only for server capacity that you need or want.
# How Amazon EC2 works

![EC2 works](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2tj3Qsu4SQiY90LLuBkIVA_c31e1445900c47cc93b0c83ff6973349_How_EC2_works.png?expiry=1665446400000&hmac=fo4TmhsiSZXpiDKDKy_QkMAUEMW0YGDxD8Q_KYia1JI)
## Launch
Begin by selecting a template with basic configurations for your instance. These configurations include the operating system, application server, or applications. You also select the instance type, which is the specific hardware configuration of your instance.As you are preparing to launch an instance, you specify security settings to control the network traffic that can flow into and out of your instance.

## Connect
You can connect to the instance in several ways. Your programs and applications have multiple different methods to connect directly to the instance and exchange data. Users can also connect to the instance by logging in and accessing the computer desktop.

## Use
You can run commands to install software, add storage, copy and organize files, and more.

# [Amazon EC2 instance types](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/b4pix/amazon-ec2-instance-types)
Amazon EC2 instance types are optimized for different tasks. When selecting an instance type, consider the specific needs of your workloads and applications. This might include requirements for compute, memory, or storage capabilities.
* **General purpose instances**(provide a balance of compute, memory, and networking resources. You can use them for a variety of workloads, such as application servers,gaming servers,backend servers for enterprise applications,small and medium databases)
* **Compute optimized instances**(Compute optimized instances are ideal for compute-bound applications that benefit from high-performance processors. Like general purpose instances, you can use compute optimized instances for workloads such as web, application, and gaming servers)
* **Memory optimized instances**(are designed to deliver fast performance for workloads that process large datasets in memory. In computing, memory is a temporary storage area. It holds all the data and instructions that a central processing unit (CPU) needs to be able to complete actions.Suppose that you have a workload that requires large amounts of data to be preloaded before running an application)
* **Accelerated computing instances**(use hardware accelerators, or coprocessors, to perform some functions more efficiently than is possible in software running on CPUs. Examples of these functions include floating-point number calculations, graphics processing, and data pattern matching)
* **Storage optimized instances**(are designed for workloads that require high, sequential read and write access to large datasets on local storage. Examples of workloads suitable for storage optimized instances include distributed file systems, data warehousing applications, and high-frequency online transaction processing (OLTP) systems)

# [Amazon EC2 Pricing](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/0tGqG/amazon-ec2-pricing)
* **On-Demand**(are ideal for short-term, irregular workloads that cannot be interrupted. No upfront costs or minimum contracts apply. The instances run continuously until you stop them, and you pay for only the compute time you use.Sample use cases for On-Demand Instances include developing and testing applications and running applications that have unpredictable usage patterns. On-Demand Instances are not recommended for workloads that last a year or longer because these workloads can experience greater cost savings using Reserved Instances)

* Amazon EC2 Savings Plans
AWS offers Savings Plans for several compute services, including Amazon EC2. Amazon EC2 Savings Plans enable you to reduce your compute costs by committing to a consistent amount of compute usage for a 1-year or 3-year term. This term commitment results in savings of up to 72% over On-Demand costs.Any usage up to the commitment is charged at the discounted Savings Plan rate (for example, $10 an hour). Any usage beyond the commitment is charged at regular On-Demand rates.

* **Reserved Instances**(are a billing discount applied to the use of On-Demand Instances in your account. You can purchase Standard Reserved and Convertible Reserved Instances for a 1-year or 3-year term, and Scheduled Reserved Instances for a 1-year term. You realize greater cost savings with the 3-year option

* **Spot Instances**(are ideal for workloads with flexible start and end times, or that can withstand interruptions. Spot Instances use unused Amazon EC2 computing capacity and offer you cost savings at up to 90% off of On-Demand pricesSuppose that you have a background processing job that can start and stop as needed (such as the data processing job for a customer survey))

* **Dedicated Hosts**(are physical servers with Amazon EC2 instance capacity that is fully dedicated to your use)

# [Scaling Amazon EC2 part 1](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/yeBLH/scaling-amazon-ec2-part-1)
Scalability involves beginning with only the resources you need and designing your architecture to automatically respond to changing demand by scaling out or in. As a result, you pay for only the resources you use. You don’t have to worry about a lack of computing capacity to meet your customers’ needs.

# Amazon EC2 Auto Scaling
If you’ve tried to access a website that wouldn’t load and frequently timed out, the website might have received more requests than it was able to handle. This situation is similar to waiting in a long line at a coffee shop, when there is only one barista present to take orders from customers.
![EC2 Auto Scaling](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/u65VmTaEQy6uVZk2hEMumA_ac1097647f974a83a7f35268af39f829_Amazon-EC2-Autoscaling.png?expiry=1665446400000&hmac=62Q0ZRdl7zX_c9VUsoeO0speFqhwQHrIOf8MpxEz5zY)
Amazon EC2 Auto Scaling enables you to automatically add or remove Amazon EC2 instances in response to changing application demand. By automatically scaling your instances in and out as needed, you are able to maintain a greater sense of application availability.

Within Amazon EC2 Auto Scaling, you can use two approaches:
* **Dynamic scaling** responds to changing demand. 
* **Predictive scaling** automatically schedules the right number of Amazon EC2 instances based on predicted demand.

# [Scaling Amazon EC2 (Part 2)](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/i8o4K/scaling-amazon-ec2-part-2)
In the cloud, computing power is a programmatic resource, so you can take a more flexible approach to the issue of scaling. By adding Amazon EC2 Auto Scaling to an application, you can add new instances to the application when necessary and terminate them when no longer needed.
Suppose that you are preparing to launch an application on Amazon EC2 instances. When configuring the size of your Auto Scaling group, you might set the minimum number of Amazon EC2 instances at one. This means that at all times, there must be at least one Amazon EC2 instance running.
![Scaling Amazon EC2](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/2PuZY-0ZTee7mWPtGU3nEQ_6a0c4f91b4f540e0b73d52099baf2369_auto_scaling_group.png?expiry=1665446400000&hmac=_UCShOATzug__O6vHWaRVpvMFqCieC1M7axWoT2OS9s)
When you create an Auto Scaling group, you can set the **minimum number** of Amazon EC2 instances. The minimum capacity is the number of Amazon EC2 instances that launch immediately after you have created the Auto Scaling group. In this example, the Auto Scaling group has a minimum capacity of one Amazon EC2 instance.
Next, you can set the **desired capacity** at two Amazon EC2 instances even though your application needs a minimum of a single Amazon EC2 instance to run.
Note: If you do not specify the desired number of Amazon EC2 instances in an Auto Scaling group, the desired capacity defaults to your minimum capacity.
The third configuration that you can set in an Auto Scaling group is the **maximum capacity**. For example, you might configure the Auto Scaling group to scale out in response to increased demand, but only to a maximum of four Amazon EC2 instances.
Because Amazon EC2 Auto Scaling uses Amazon EC2 instances, you pay for only the instances you use, when you use them. You now have a cost-effective architecture that provides the best customer experience while reducing expenses.

# [Elastic Load Balancer](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/ggIG6/elastic-load-balancer)
A load balancer acts as a single point of contact for all incoming web traffic to your Auto Scaling group. This means that as you add or remove Amazon EC2 instances in response to the amount of incoming traffic, these requests route to the load balancer first. Then, the requests spread across multiple resources that will handle them. For example, if you have multiple Amazon EC2 instances, Elastic Load Balancing distributes the workload across the multiple instances so that no single instance has to carry the bulk of it.Although Elastic Load Balancing and Amazon EC2 Auto Scaling are separate services, they work together to help ensure that applications running in Amazon EC2 can provide high performance and availability. 

Example: **Elastic Load Balancing**
## Low-demand period
Suppose that a few customers have come to the coffee shop and are ready to place their orders. 

If only a few registers are open, this matches the demand of customers who need service. The coffee shop is less likely to have open registers with no customers. In this example, you can think of the registers as Amazon EC2 instances.
![Low-demand period](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uBpHtGayR36aR7Rmsqd-iQ_358a78c039944740b7a09d8c6a3b25ba_ELB.png?expiry=1665446400000&hmac=MXgYzUgjetXqpMn0INPKJ-Mj5TeXVNFJ7z6-AkWO-qI)

## High-demand period
Throughout the day, as the number of customers increases, the coffee shop opens more registers to accommodate them. In the diagram, the Auto Scaling group represents this.Additionally, a coffee shop employee directs customers to the most appropriate register so that the number of requests can evenly distribute across the open registers. You can think of this coffee shop employee as a load balancer. 
![High-demand period](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/X_olcKCYS-e6JXCgmPvn1A_bcf653ef221649bda401adead0a0fa70_ELB_2.png?expiry=1665446400000&hmac=3MXHBbMgvSCcmfCCUJW1SMETUfqstjBpCrcov7EE6MY)

# [Monolithic Applications and Microservices](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/zPgHL/monolithic-applications-and-microservices)
## Monolithic
Applications are made of multiple components. The components communicate with each other to transmit data, fulfill requests, and keep the application running. 
Suppose that you have an application with tightly coupled components. These components might include databases, servers, the user interface, business logic, and so on. This type of architecture can be considered a monolithic application. 
In this approach to application architecture, if a single component fails, other components fail, and possibly the entire application fails.
![Monolithic Applications](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/oy3xh1bhR3at8YdW4Td2iQ_a3cace5aff3f43509c25a520596d3615_monolithic.png?expiry=1665446400000&hmac=OAk7zLTZ-Vz26Hl1ATXX_vrC40VT6L73DqiCavgoYlI)
## Microservices
To help maintain application availability when a single component fails, you can design your application through a microservices approach.
In a microservices approach, application components are loosely coupled. In this case, if a single component fails, the other components continue to work because they are communicating with each other. The loose coupling prevents the entire application from failing.When designing applications on AWS, you can take a microservices approach with services and components that fulfill different functions. Two services facilitate application integration: Amazon Simple Notification Service (Amazon SNS) and Amazon Simple Queue Service (Amazon SQS).

# [Amazon Simple Notification Service (Amazon SNS)](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/nbtmX/amazon-simple-notification-service-amazon-sns)
Amazon Simple Notification Service (Amazon SNS) is a publish/subscribe service. Using Amazon SNS topics, a publisher publishes messages to subscribers. This is similar to the coffee shop; the cashier provides coffee orders to the barista who makes the drinks.
In Amazon SNS, subscribers can be web servers, email addresses, AWS Lambda functions, or several other options.
Publishing updates from a single topic
![Amazon SNS](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/d0Bqy4uDSfmAasuLg4n5tw_da7b81dab488441fbad62388a903b680_SNS.png?expiry=1665446400000&hmac=JTgepaJg-hD9IG1i2wTYtwIfXdTCAF8xaFarjAemFfc)
Suppose that the coffee shop has a single newsletter that includes updates from all areas of its business. It includes topics such as coupons, coffee trivia, and new products. All of these topics are grouped because this is a single newsletter. All customers who subscribe to the newsletter receive updates about coupons, coffee trivia, and new products.After a while, some customers express that they would prefer to receive separate newsletters for only the specific topics that interest them. The coffee shop owners decide to try this approach.
Publishing updates from multiple topics
![multiple topics](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/o5cw7G1JRkCXMOxtSWZABw_64ad2718f82440699467fccecc81445c_SNS_2.png?expiry=1665446400000&hmac=0JXuDTXPGEZoiPHTUCoDfQFm0m_u_ufYJVn1VdeXUyo)
Now, instead of having a single newsletter for all topics, the coffee shop has broken it up into three separate newsletters. Each newsletter is devoted to a specific topic: coupons, coffee trivia, and new products.Subscribers will now receive updates immediately for only the specific topics to which they have subscribed.
It is possible for subscribers to subscribe to a single topic or to multiple topics. For example, the first customer subscribes to only the coupons topic, and the second subscriber subscribes to only the coffee trivia topic. The third customer subscribes to both the coffee trivia and new products topics.

# [Amazon Simple Queue Service (Amazon SQS)](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/AW8HH/amazon-simple-queue-service-amazon-sqs)
Using Amazon SQS, you can send, store, and receive messages between software components, without losing messages or requiring other services to be available. In Amazon SQS, an application sends messages into a queue. A user or service retrieves a message from the queue, processes it, and then deletes it from the queue.
![Simple Queue Service](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/y8UXj-I9TSCFF4_iPa0gPw_57c347cc1e3d432b8553665d9bc49150_SQS_1.png?expiry=1665446400000&hmac=wDssHBx6loQSr3hHH5VXyh-A_8QceZ5ubqYSuW3bMLs)
Suppose that the coffee shop has an ordering process in which a cashier takes orders, and a barista makes the orders. Think of the cashier and the barista as two separate components of an application. 

First, the cashier takes an order and writes it down on a piece of paper. Next, the cashier delivers the paper to the barista. Finally, the barista makes the drink and gives it to the customer.
When the next order comes in, the process repeats. This process runs smoothly as long as both the cashier and the barista are coordinated.
What might happen if the cashier took an order and went to deliver it to the barista, but the barista was out on a break or busy with another order? The cashier would need to wait until the barista is ready to accept the order. This would cause delays in the ordering process and require customers to wait longer to receive their orders.As the coffee shop has become more popular and the ordering line is moving more slowly, the owners notice that the current ordering process is time consuming and inefficient. They decide to try a different approach that uses a queue.
![Orders in a queue](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/j4F0N9soTamBdDfbKB2pXQ_d4548eb733f24c7f89fa1256637d0da6_SQS_2.jpg?expiry=1665446400000&hmac=R6jx58dH9-9avQkRF2C7P3XaVbOzzwJOeU3qbQfCQJw)
Recall that the cashier and the barista are two separate components of an application. A message queuing service such as Amazon SQS enables messages between decoupled application components.

The cashier puts the order into a queue. You can think of this as an order board that serves as a buffer between the cashier and the barista. Even if the barista is out on a break or busy with another order, the cashier can continue placing new orders into the queue. Next, the barista checks the queue and retrieves the order.The barista prepares the drink and gives it to the customer.The barista then removes the completed order from the queue.While the barista is preparing the drink, the cashier is able to continue taking new orders and add them to the queue.
# [Serverless Computing](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/5q8hS/serverless-computing)
If you have applications that you want to run in Amazon EC2, you must do the following:
1) Provision instances (virtual servers).
2) Upload your code
3) Continue to manage the instances while your application is running.
![Serverless Computing](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4CCw_UNETnygsP1DRM58WQ_b8c1c87562fc4cd3adcb3bd08bece012_Serverless-Computing.png?expiry=1665446400000&hmac=WvEAHe5-2X_o5CXHKsajnIxluM5kOu_EX1KTGKADDxY)
The term “serverless” means that your code runs on servers, but you do not need to provision or manage these servers. With serverless computing, you can focus more on innovating new products and features instead of maintaining servers.

**AWS Lambda** is a service that lets you run code without needing to provision or manage servers. 
While using AWS Lambda, you pay only for the compute time that you consume. Charges apply only when your code is running. You can also run code for virtually any type of application or backend service, all with zero administration. 
For example, a simple Lambda function might involve automatically resizing uploaded images to the AWS Cloud. In this case, the function triggers when uploading a new image. 
![AWS Lambda](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/aFDLTd29SHSQy03dvZh02w_14639fa7da6e4e7f895ffb6720671934_Lambda.png?expiry=1665446400000&hmac=Wat3yL5xsWPFmuAZJnjpJ7muQfjdxz435ZykGaGMFp0)
* You upload your code to Lambda.
* You set your code to trigger from an event source, such as AWS services, mobile applications, or HTTP endpoints.
* Lambda runs your code only when triggered.
* You pay only for the compute time that you use.
## Containers
In AWS, you can also build and run containerized applications.Containers provide you with a standard way to package your application's code and dependencies into a single object. You can also use containers for processes and workflows in which there are essential requirements for security, reliability, and scalability.
![One host with multiple containers](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/hP-3PaWVR1a_tz2llbdWRQ_3616a8a1e54545c3ab4e42469c4559e2_Containers1.png?expiry=1665446400000&hmac=hQbFLIh9Gb_u7PtYaLofNat1krozit9tWArja53qhAA)
Suppose that a company’s application developer has an environment on their computer that is different from the environment on the computers used by the IT operations staff. The developer wants to ensure that the application’s environment remains consistent regardless of deployment, so they use a containerized approach. This helps to reduce time spent debugging applications and diagnosing differences in computing environments.
![Containers](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/eJ0dRbpYQbmdHUW6WIG5DQ_75fdd82e8d014bef831d39b0122ed901_Containers2.png?expiry=1665446400000&hmac=XyRtjtnRlZcxTRtdOKgKq-XrVS0a4GeI_jrVUFj4fSU)
When running containerized applications, it’s important to consider scalability. Suppose that instead of a single host with multiple containers, you have to manage tens of hosts with hundreds of containers. Alternatively, you have to manage possibly hundreds of hosts with thousands of containers. At a large scale, imagine how much time it might take for you to monitor memory usage, security, logging, and so on.
## Amazon Elastic Container Service (Amazon ECS)
Amazon Elastic Container Service (Amazon ECS) is a highly scalable, high-performance container management system that enables you to run and scale containerized applications on AWS.Amazon ECS supports Docker containers. Docker is a software platform that enables you to build, test, and deploy applications quickly. AWS supports the use of open-source Docker Community Edition and subscription-based Docker Enterprise Edition. With Amazon ECS, you can use API calls to launch and stop Docker-enabled applications.
