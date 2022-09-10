Task name: AWS Regions, Availability Zones, Edge Locations(About, List, characteristics)

[Resource](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)

> Date:7-sep-2022
---
# Regions
Each Region is designed to be isolated from the other Regions. This achieves the greatest possible fault tolerance and stability.
When you view your resources, you see only the resources that are tied to the Region that you specified. This is because Regions are isolated from each other, and we don't automatically replicate resources across Regions.
When you launch an instance, you must select an AMI that's in the same Region. If the AMI is in another Region, you can copy the AMI to the Region you're using.

|Code	Name|	Opt-in| Status|
|:-----------:|:-------------:|:--------------:|
|us-east-2	|US East (Ohio)	|Not required|
|us-east-1	|US East (N. Virginia)	|Not required|
|us-west-1	|US West (N. California)	|Not required|
|us-west-2	|US West (Oregon)	|Not required|
|af-south-1	|Africa (Cape Town)	|Required|
|ap-east-1	|Asia Pacific (Hong Kong)	|Required|
|ap-southeast-3	|Asia Pacific (Jakarta)	|Required|
|ap-south-1	|Asia Pacific (Mumbai)	|Not required|
|ap-northeast-3	|Asia Pacific (Osaka)	|Not required|
|ap-northeast-2	|Asia Pacific (Seoul)	|Not required|
|ap-southeast-1	|Asia Pacific (Singapore)	|Not required|
|ap-southeast-2	|Asia Pacific (Sydney)	|Not required|
|ap-northeast-1	|Asia Pacific (Tokyo)	|Not required|
|ca-central-1	|Canada (Central)	|Not required|
|eu-central-1	|Europe (Frankfurt)	|Not required|
|eu-west-1	|Europe (Ireland)	|Not required|
|eu-west-2	|Europe (London)	|Not required|
|eu-south-1	|Europe (Milan)	|Required|
|eu-west-3	|Europe (Paris)	|Not required|
|eu-north-1	|Europe (Stockholm)	|Not required|
|me-south-1	|Middle East (Bahrain)	|Required|
|me-central-1|	Middle East (UAE)	|Required|
|sa-east-1|	South America (São Paulo)	|Not required|


# Availability Zones
Each Region has multiple, isolated locations known as Availability Zones. The code for Availability Zone is its Region code followed by a letter identifier. For example, us-east-1a.
When you launch an instance, you select a Region and a virtual private cloud (VPC), and then you can either select a subnet from one of the Availability Zones or let us choose one for you. If you distribute your instances across multiple Availability Zones and one instance fails, you can design your application so that an instance in another Availability Zone can handle requests. You can also use Elastic IP addresses to mask the failure of an instance in one Availability Zone by rapidly remapping the address to an instance in another Availability Zone.
As Availability Zones grow over time, our ability to expand them can become constrained. If this happens, we might restrict you from launching an instance in a constrained Availability Zone unless you already have an instance in that Availability Zone. Eventually, we might also remove the constrained Availability Zone from the list of Availability Zones for new accounts. Therefore, your account might have a different number of available Availability Zones in a Region than another account.

# Local Zones
A Local Zone is an extension of an AWS Region in geographic proximity to your users. Local Zones have their own connections to the internet and support AWS Direct Connect, so that resources created in a Local Zone can serve local users with low-latency communications.
The code for a Local Zone is its Region code followed by an identifier that indicates its physical location. For example, us-west-2-lax-1 in Los Angeles.

US East (N. Virginia) Local Zones

The following table lists Local Zones in US East (N. Virginia):

|Parent Region	|Zone Name	|Location (metro area)|
|:-------------------:|:--------------:|:-------------:|
|US East (N. Virginia)	|us-east-1-atl-1a	|Atlanta|
|US East (N. Virginia)	|us-east-1-bos-1a	|Boston|
|US East (N. Virginia)	|us-east-1-chi-1a	|Chicago|
|US East (N. Virginia)	|us-east-1-dfw-1a	|Dallas|
|US East (N. Virginia)	|us-east-1-iah-1a	|Houston|
|US East (N. Virginia)	|us-east-1-mci-1a	|Kansas City|
|US East (N. Virginia)	|us-east-1-mia-1a	|Miami|
|US East (N. Virginia)	|us-east-1-msp-1a	|Minneapolis|
|US East (N. Virginia)	|us-east-1-nyc-1a	|New York City|
|US East (N. Virginia)	|us-east-1-phl-1a	|Philadelphia|

US West (Oregon) Local Zones

The following table lists Local Zones in US West (Oregon):

|Parent Region	|Zone Name	|Location (metro area)|
|:-------------:|:----------------:|:----------:|
|US West (Oregon)	|us-west-2-den-1a	|Denver|
|US West (Oregon)	|us-west-2-las-1a	|Las Vegas|
|US West (Oregon)	|us-west-2-lax-1a	|Los Angeles|
|US West (Oregon)	|us-west-2-lax-1b	|Los Angeles|
|US West (Oregon)	|us-west-2-phx-1a	|Phoenix|
|US West (Oregon)	|us-west-2-pdx-1a	|Portland|
|US West (Oregon)	|us-west-2-sea-1a	|Seattle|


# Wavelength Zones
AWS Wavelength enables developers to build applications that deliver ultra-low latencies to mobile devices and end users. Wavelength deploys standard AWS compute and storage services to the edge of telecommunication carriers' 5G networks. Developers can extend a virtual private cloud (VPC) to one or more Wavelength Zones, and then use AWS resources like Amazon EC2 instances to run applications that require ultra-low latency and a connection to AWS services in the Region.
A Wavelength Zone is an isolated zone in the carrier location where the Wavelength infrastructure is deployed. Wavelength Zones are tied to a Region. A Wavelength Zone is a logical extension of a Region, and is managed by the control plane in the Region.
The code for a Wavelength Zone is its Region code followed by an identifier that indicates the physical location. For example, us-east-1-wl1-bos-wlz-1 in Boston.

# AWS Outposts
AWS Outposts is a fully managed service that extends AWS infrastructure, services, APIs, and tools to customer premises. By providing local access to AWS managed infrastructure, AWS Outposts enables customers to build and run applications on premises using the same programming interfaces as in AWS Regions, while using local compute and storage resources for lower latency and local data processing needs.
An Outpost is a pool of AWS compute and storage capacity deployed at a customer site. AWS operates, monitors, and manages this capacity as part of an AWS Region. You can create subnets on your Outpost and specify them when you create AWS resources. Instances in Outpost subnets communicate with other instances in the AWS Region using private IP addresses, all within the same VPC.


