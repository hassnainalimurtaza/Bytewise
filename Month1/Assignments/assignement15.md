# Task Name: What is AWS Well-Architecture Framework, Describe Extensively along with benefits?, How can you be innovative on AWS?

[AWS Well-Architected Framework]( https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html)

[Innovation with AWS](https://aws.amazon.com/innovation/)

>  Date:21-sep-2022
--- 
# AWS Well-Architected Framework 
The AWS Well-Architected Framework helps you understand the pros and cons of decisions you make while building systems on AWS. Using the Framework helps you learn architectural best practices for designing and operating secure, reliable, efficient, cost-effective, and sustainable workloads in the AWS Cloud. It provides a way for you to consistently measure your architectures against best practices and identify areas for improvement. The process for reviewing an architecture is a constructive conversation about architectural decisions, and is not an audit mechanism. We believe that having well-architected systems greatly increases the likelihood of business success.
AWS Solutions Architects have years of experience architecting solutions across a wide variety of business verticals and use cases. We have helped design and review thousands of customers’ architectures on AWS. From this experience, we have identified best practices and core strategies for architecting systems in the cloud.
Name	Description
Operational Excellence	The ability to support development and run workloads effectively, gain insight into their operations, and to continuously improve supporting processes and procedures to deliver business value.
Security	The security pillar describes how to take advantage of cloud technologies to protect data, systems, and assets in a way that can improve your security posture.
Reliability	The reliability pillar encompasses the ability of a workload to perform its intended function correctly and consistently when it’s expected to. This includes the ability to operate and test the workload through its total lifecycle. This paper provides in-depth, best practice guidance for implementing reliable workloads on AWS.
Performance Efficiency	The ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve.
Cost Optimization	The ability to run systems to deliver business value at the lowest price point.
Sustainability	The ability to continually improve sustainability impacts by reducing energy consumption and increasing efficiency across all components of a workload by maximizing the benefits from the provisioned resources and minimizing the total resources required.

## Operational Excellence
The Operational Excellence pillar includes the ability to support development and run workloads effectively, gain insight into their operations, and to continuously improve supporting processes and procedures to deliver business value. 
The operational excellence pillar provides an overview of design principles, best practices, and questions. You can find prescriptive guidance on implementation in the Operational Excellence Pillar whitepaper.
* ### Organization
Your teams need to have a shared understanding of your entire workload, their role in it, and shared business goals to set the priorities that will enable business success. Well-defined priorities will maximize the benefits of your efforts.
* ### Prepare
To prepare for operational excellence, you have to understand your workloads and their expected behaviors. You will then be able to design them to provide insight to their status and build the procedures to support them.
* ### Operate
Successful operation of a workload is measured by the achievement of business and customer outcomes. Define expected outcomes, determine how success will be measured, and identify metrics that will be used in those calculations to determine if your workload and operations are successful
* ### Evolve
You must learn, share, and continuously improve to sustain operational excellence. Dedicate work cycles to making continuous incremental improvements.



## Security
To operate your workload securely, you must apply overarching best practices to every area of security. Take requirements and processes that you have defined in operational excellence at an organizational and workload level, and apply them to all areas.
* ### Identity and Access Management
Identity and access management are key parts of an information security program, ensuring that only authorized and authenticated users and components are able to access your resources, and only in a manner that you intend
* ### Detection
You can use detective controls to identify a potential security threat or incident. They are an essential part of governance frameworks and can be used to support a quality process, a legal or compliance obligation, and for threat identification and response efforts.
* ### Infrastructure Protection
Infrastructure protection encompasses control methodologies, such as defense in depth, necessary to meet best practices and organizational or regulatory obligations.
* ### Data Protection
Before architecting any system, foundational practices that influence security should be in place. For example, data classification provides a way to categorize organizational data based on levels of sensitivity, and encryption protects data by way of rendering it unintelligible to unauthorized access
* ### Incident Response
Even with extremely mature preventive and detective controls, your organization should still put processes in place to respond to and mitigate the potential impact of security incidents. 

## Reliability
The Reliability pillar encompasses the ability of a workload to perform its intended function correctly and consistently when it’s expected to. This includes the ability to operate and test the workload through its total lifecycle.
* ### Foundations
Foundational requirements are those whose scope extends beyond a single workload or project. Before architecting any system, foundational requirements that influence reliability should be in place.
* ### Workload Architecture
A reliable workload starts with upfront design decisions for both software and infrastructure. Your architecture choices will impact your workload behavior across all of the Well-Architected pillars
* ### Change Management
Changes to your workload or its environment must be anticipated and accommodated to achieve reliable operation of the workload. Changes include those imposed on your workload, such as spikes in demand, as well as those from within, such as feature deployments and security patches.
* ### Failure Management
In any system of reasonable complexity, it is expected that failures will occur. Reliability requires that your workload be aware of failures as they occur and take action to avoid impact on availability.

## Performance Efficiency
The Performance Efficiency pillar includes the ability to use computing resources efficiently to meet system requirements, and to maintain that efficiency as demand changes and technologies evolve.
* ### Selection
The optimal solution for a particular workload varies, and solutions often combine multiple approaches. Well-architected workloads use multiple solutions and enable different features to improve performance.
* ### Review
Cloud technologies are rapidly evolving and you must ensure that workload components are using the latest technologies and approaches to continually improve performance.
* ### Monitoring
After you implement your workload, you must monitor its performance so that you can remediate any issues before they impact your customers. Monitoring metrics should be used to raise alarms when thresholds are breached.
* ### Tradeoffs
When you architect solutions, think about tradeoffs to ensure an optimal approach. Depending on your situation, you could trade consistency, durability, and space for time or latency, to deliver higher performance.
## Cost Optimization
The Cost Optimization pillar includes the ability to run systems to deliver business value at the lowest price point.
* ### Practice Cloud Financial Management
With the adoption of cloud, technology teams innovate faster due to shortened approval, procurement, and infrastructure deployment cycles. A new approach to financial management in the cloud is required to realize business value and financial success. 
* ### Expenditure and usage awareness
The increased flexibility and agility that the cloud enables encourages innovation and fast-paced development and deployment. It eliminates the manual processes and time associated with provisioning on-premises infrastructure, including identifying hardware specifications, negotiating price quotations, managing purchase orders, scheduling shipments, and then deploying the resources. However, the ease of use and virtually unlimited on-demand capacity requires a new way of thinking about expenditures.
* ### Cost-effective resources
Using the appropriate instances and resources for your workload is key to cost savings. For example, a reporting process might take five hours to run on a smaller server but one hour to run on a larger server that is twice as expensive. Both servers give you the same outcome, but the smaller server incurs more cost over time.
* ### Manage demand and supply resources
When you move to the cloud, you pay only for what you need. You can supply resources to match the workload demand at the time they’re needed, this eliminates the need for costly and wasteful over provisioning
* ### Optimize over time
As AWS releases new services and features, it's a best practice to review your existing architectural decisions to ensure they continue to be the most cost effective.
## Sustainability
The Sustainability pillar focuses on environmental impacts, especially energy consumption and efficiency, since they are important levers for architects to inform direct action to reduce resource usage.
* ### Region selection
Choose Regions where you will implement your workloads based on both your business requirements and sustainability goals.
* ### User behavior patterns
The way users consume your workloads and other resources can help you identify improvements to meet sustainability goals.
* ### Software and architecture patterns
Implement patterns for performing load smoothing and maintaining consistent high utilization of deployed resources to minimize the resources consumed. 
* ### Data Patterns
Implement patterns for performing load smoothing and maintaining consistent high utilization of deployed resources to minimize the resources consumed.
* ### Hardware patterns
Look for opportunities to reduce workload sustainability impacts by making changes to your hardware management practices.
* ### Development and deployment patterns
Look for opportunities to reduce your sustainability impact by making changes to your development, test, and deployment practices.

# Innovation with AWS
AWS helps you use the cloud to turn ideas into opportunities—creating new ways to grow, increase efficiency, and serve customers better. Our customer-obsessed culture, industry-leading cloud services, and global customer and partner community offer a unique set of tools and expertise for solving problems and exploring possibilities.
