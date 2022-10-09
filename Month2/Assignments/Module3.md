# [Regions](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/lecture/pXq5y/regions)
# [Selecting a Region](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/TfxPi/selecting-a-region)
* Compliance with data governance and legal requirements(Depending on your company and location, you might need to run your data out of specific areas)
* Proximity to your customers(Selecting a Region that is close to your customers will help you to get content to them faster)
* Available services within a Region(AWS is frequently innovating by creating new services and expanding on features within existing services)
* Pricing(the cost of services can vary from Region to Region)
# [Availability Zones](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/uYynk/availability-zones)
![[Availability Zones](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/4Nn3-avkQfeZ9_mr5IH3Qg_6ff859ac606549e492cfa32a46d95438_AZ1.png?expiry=1665446400000&hmac=UKQfhSX6IL0kMDnmLbDUXY4srXnsjsJHsQFg_yvnFwE)

An Availability Zone is a single data center or a group of data centers within a Region. Availability Zones are located tens of miles apart from each other. This is close enough to have low latency (the time between when content requested and received) between Availability Zones. However, if a disaster occurs in one part of the Region, they are distant enough to reduce the chance that multiple Availability Zones are affected.

# [Edge Locations](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/zOomb/edge-locations)
An edge location is a site that Amazon CloudFront uses to store cached copies of your content closer to your customers for faster delivery.
![Edge Locations](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/-a9Jewz_SECvSXsM_4hArA_e79997e9255644d3ac232ea0bc3c5598_EdgeLocations1.png?expiry=1665446400000&hmac=vjfIdDVH-mI8crWbVtvAbU5KH9WPogU2NUrVPQYzmWc)

* Origin(don’t need to move all the content to one of the Regions)
* Edge Location(cache a copy locally at an edge location that is close to your customers)
* Customer(customer in China requests one of your files, Amazon CloudFront retrieves the file from the cache in the edge location and delivers the file to the customer)

# [Ways to Interact with AWS Services](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/5GoWn/ways-to-interact-with-aws-services)
## AWS Management Console
![AWS Management Console](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/hF4BjX0NSgaeAY19DeoGRg_ee2edbfb776b4a28ab3930a9d53bec8f_Ways-to-interact1.png?expiry=1665446400000&hmac=AjD8vjso_V9Kmc-O5PGSIX-5ejaKRvb7MqDQLfOZ0_M)

The AWS Management Console is a web-based interface for accessing and managing AWS services. You can quickly access recently used services and search for other services by name, keyword, or acronym. The console includes wizards and automated workflows that can simplify the process of completing tasks.

## AWS Command Line Interface
![AWS Command Line Interface](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/bz4GteTiSZO-BrXk4nmTzA_f210f1b2c5d34d91850ff7ec52aebe05_Ways-to-interact2.png?expiry=1665446400000&hmac=KtFKeewM1psHtvECyBm832ooKVJ8yjimAOmP-ODz8nM)

To save time when making API requests, you can use the AWS Command Line Interface (AWS CLI). AWS CLI enables you to control multiple AWS services directly from the command line within one tool. AWS CLI is available for users on Windows, macOS, and Linux. 

## Software development kits (SDKs)
![SDK](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/elP4JbJ5RqiT-CWyeUaopw_9954e0abfd7547ba8001a55c3996dca4_Ways-to-interact3.png?expiry=1665446400000&hmac=wSTAVj2ckSONjtH4z6HH_Z15DUOL4jx4zwtBlRiATKQ)

Another option for accessing and managing AWS services is the software development kits (SDKs). SDKs make it easier for you to use AWS services through an API designed for your programming language or platform. SDKs enable you to use AWS services with your existing applications or create entirely new applications that will run on AWS

# [AWS Elastic Beanstalk and AWS CloudFormation](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/UuoXx/aws-elastic-beanstalk-and-aws-cloudformation)

## AWS Elastic Beanstalk
With AWS Elastic Beanstalk, you provide code and configuration settings, and Elastic Beanstalk deploys the resources necessary to perform the following tasks:
* Adjust capacity
* Load balancing
* Automatic scaling
* Application health monitoring

## AWS CloudFormation
With AWS CloudFormation, you can treat your infrastructure as code. This means that you can build an environment by writing lines of code instead of using the AWS Management Console to individually provision resources.
