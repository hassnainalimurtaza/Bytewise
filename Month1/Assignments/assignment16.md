# Task name: Subnets and Network Access Control list in general and in context with AWS Guide, Global Networking in AWS

[Control traffic to subnets using Network ACLs](https://docs.aws.amazon.com/vpc/latest/userguide/vpc-network-acls.html#nacl-basics)

[Global networks](https://docs.aws.amazon.com/vpc/latest/tgwnm/global-networks.html)

> Date:22-sep-22
---
# Control traffic to subnets using Network ACLs
A network access control list (ACL) allows or denies specific inbound or outbound traffic at the subnet level. You can use the default network ACL for your VPC, or you can create a custom network ACL for your VPC with rules that are similar to the rules for your security groups in order to add an additional layer of security to your VPC.
* Your VPC automatically comes with a modifiable default network ACL. By default, it allows all inbound and outbound IPv4 traffic and, if applicable, IPv6 traffic.
* You can create a custom network ACL and associate it with a subnet. By default, each custom network ACL denies all inbound and outbound traffic until you add rules.
* Each subnet in your VPC must be associated with a network ACL. If you don't explicitly associate a subnet with a network ACL, the subnet is automatically associated with the default network ACL.
* You can associate a network ACL with multiple subnets. However, a subnet can be associated with only one network ACL at a time. When you associate a network ACL with a subnet, the previous association is removed.
* A network ACL has inbound rules and outbound rules. Each rule can either allow or deny traffic. Each rule has a number 1 from to 32766.
* We evaluate the network ACL rules when traffic enters and leaves the subnet, not as it is routed within a subnet.
* Network ACLs are stateless, which means that responses to allowed inbound traffic are subject to the rules for outbound traffic (and vice versa).
## Network ACL rules
You can add or remove rules from the default network ACL, or create additional network ACLs for your VPC. When you add or remove rules from a network ACL, the changes are automatically applied to the subnets that it's associated with.
* Rule number. Rules are evaluated starting with the lowest numbered rule. As soon as a rule matches traffic, it's applied regardless of any higher-numbered rule that might contradict it.
* Type. The type of traffic; for example, SSH. You can also specify all traffic or a custom range.
* Protocol. You can specify any protocol that has a standard protocol number. For more information, see Protocol Numbers. If you specify ICMP as the protocol, you can specify any or all of the ICMP types and codes.
* Port range. The listening port or port range for the traffic. For example, 80 for HTTP traffic.
* Source. [Inbound rules only] The source of the traffic (CIDR range).
* Destination. [Outbound rules only] The destination for the traffic (CIDR range).
* Allow/Deny. Whether to allow or deny the specified traffic.
## Default network ACL
The default network ACL is configured to allow all traffic to flow in and out of the subnets with which it is associated. Each network ACL also includes a rule whose rule number is an asterisk. This rule ensures that if a packet doesn't match any of the other numbered rules, it's denied. You can't modify or remove this rule.
## Custom network ACL
The following table shows an example of a custom network ACL for a VPC that supports IPv4 only. It includes rules that allow HTTP and HTTPS traffic in (inbound rules 100 and 110). There's a corresponding outbound rule that enables responses to that inbound traffic (outbound rule 140, which covers ephemeral ports 32768-65535)
## Custom network ACLs and other AWS services
If you create a custom network ACL, be aware of how it might affect resources that you create using other AWS services.With Elastic Load Balancing, if the subnet for your backend instances has a network ACL in which you've added a deny rule for all traffic with a source of either 0.0.0.0/0 or the subnet's CIDR, your load balancer can't carry out health checks on the instances. For more information about the recommended network ACL rules for your load balancers and backend instances, see Network ACLs for Load Balancers in a VPC in the User Guide for Classic Load Balancers
## Ephemeral ports
The example network ACL in the preceding section uses an ephemeral port range of 32768-65535. However, you might want to use a different range for your network ACLs depending on the type of client that you're using or with which you're communicating.
The client that initiates the request chooses the ephemeral port range. The range varies depending on the client's operating system.
* Many Linux kernels (including the Amazon Linux kernel) use ports 32768-61000.
* Requests originating from Elastic Load Balancing use ports 1024-65535.
* Windows operating systems through Windows Server 2003 use ports 1025-5000.
* Windows Server 2008 and later versions use ports 49152-65535.
* A NAT gateway uses ports 1024-65535.
* AWS Lambda functions use ports 1024-65535.

## Path MTU Discovery
Path MTU Discovery is used to determine the path MTU between two devices. The path MTU is the maximum packet size that's supported on the path between the originating host and the receiving host.
For IPv4, when a host sends a packet that's larger than the MTU of the receiving host or that's larger than the MTU of a device along the path, the receiving host or device drops the packet, and then returns the following ICMP message: Destination Unreachable: Fragmentation Needed and Don't Fragment was Set (Type 3, Code 4). This instructs the transmitting host to split the payload into multiple smaller packets, and then retransmit them.
# Global Network
Performance is a key driver of the design of the AWS global infrastructure. AWS has the largest global infrastructure footprint of any cloud provider, and this footprint is expanding continuously to help customers deliver better end-user experiences, rapidly expand operations to virtually any region or country, and to meet their data locality and sovereignty requirements. If a business wishes to serve its customers in Europe, the customer should be able to choose from a broad selection of regions or data centers in Europe such as Paris, London, Frankfurt or Dublin to deliver the best possible customer experience.
## Global Infrastructure
Every data center, AZ, and AWS Region is interconnected via a purpose-built, highly available, and low-latency private global network infrastructure. The network is built on a global, fully redundant, parallel 100 GbE metro fiber network that is linked via trans-oceanic cables across the Atlantic, Pacific, and Indian Oceans, as well as the Mediterranean, Red Sea, and South China Seas.
### High Performance
Availability Zones (AZs) give customers the ability to operate production applications and databases that are more highly available, fault tolerant, and scalable than would be possible from a single data center.

### Flexible, global footprint
All Availability Zones (AZs) are interconnected with high-bandwidth, low-latency networking, over fully redundant, dedicated metro fiber providing high-throughput, low-latency networking between AZs. AZs are also powerful tools for helping build highly available applications.
