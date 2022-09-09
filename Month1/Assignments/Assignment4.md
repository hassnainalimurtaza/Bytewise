# **Task Name:** Amazon EC2 (Introduction, Types, Scaling, Auto Scaling)

[Resource](https://www.w3schools.com/aws/aws_cloudessentials_ec2intro.php)

> Date:6-SEP-2022
---
Introduction
It’s a virtual server on aws cloud, Aws Elastic Cloud Compute , scaling up and down is easy,only pay for using which resources
1. Launch
Start with selecting a template with basic configurations.
The config includes the operating system, application server, or applications.
Next, decide the instance type and hardware configuration of your instance.
Finally, specify the security settings to control the traffic in and out of your instance.
You will learn more about cloud security later in this tutorial.

2. Connect
There are many ways to connect an instance.
Programs and applications have multiple connection methods to exchange data.
Users can connect and access the computer desktop by logging in.

3. Use
Once connected, you can use the instance.
Execute commands to install software, add storage, copy, and organize files, and much more.

## Types
When selecting an instance type, consider the needs.
For example, needs can be a requirement for compute, memory, or storage.

### General Purpose Instance
The General Purpose Instance balances computing, memory, and networking resources.
It fits many purposes. Such as:
*	Application servers
*	Gaming servers
*	Backend servers for companies
*	Small and medium databases
### Compute Optimized Instances
high compute.
good for application servers, gaming servers, and web applications.
ideal for high-performance and compute-intensive needs.

### Memory Optimized Instances
deliver large dataset workloads fast.
Memory is a temporary storage area.
It loads from storage, holds the data, and processes it before the computer can run it.
The processing allows for a preloading process and gives the CPU direct access to the computer program.
The Memory Optimized Instances are best when huge amounts of data need to be preloaded before running the app.

### Accelerated Computing Instances
This type use hardware accelerators.
The accelerators boost the data processing.
The Accelerated Computing Instances are best for graphics applications and streaming.

### Storage Optimized Instances
This type is best when you have large datasets on local storage.
Some examples:
*	Large file systems
*	Data warehouses
*	Online transaction systems
The Storage Optimized Instances are designed to deliver many inputs as fast as possible.

### Scaling
Scaling is about only using the resources that you need.
In addition, have the flexibility to grow freely.
Make sure to have an architecture that can handle changes in demand.
Designing a scalable achitecture allow you to only pay for the resources that you need at any given time.

Servers can get more requests than they can handle.
Too many requests can cause timeouts and outages.
AWS EC2 Auto Scaling allows you to add or remove EC2 instances automatically.
It automates the capacity to the demand.
There are two approaches:
*	Dynamic scaling: responds to changing demand
*	Predictive scaling: schedules the number of instances based on a predicted demand
*	Dynamic and Predictive scaling can be combined to scale faster

### Auto Scaling
AWS EC2 Auto Scaling
EC2 Auto Scaling can be added as a buffer on top of your instances.
It can add new instances to the application when necessary and terminate them when no longer needed.
You can set up a group of instances.
Here you can set a minimum capacity of instances that will always be running. The rest will operate when necessary.
You can set the desired number of AWS EC2 instances in the scaling group.
However, the desired capacity defaults to your minimum capacity if not specified.
The last configuration is Maximum capacity.
Here you set the maximum capacity of instances to be used.
The Auto Scaling groups allow you to have a dynamic environment.
You set the minimum capacity, the desired number, and the maximum capacity.
The group will operate within the config and give you a predictable and cost-effective architecture.
