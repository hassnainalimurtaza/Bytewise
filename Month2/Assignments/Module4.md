# [Connectivity to AWS](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/fnPBy/connectivity-to-aws)
## Amazon Virtual Private Cloud (Amazon VPC)
A networking service that you can use to establish boundaries around your AWS resources is Amazon Virtual Private Cloud (Amazon VPC).
Amazon VPC enables you to provision an isolated section of the AWS Cloud. In this isolated section, you can launch resources in a virtual network that you define. Within a virtual private cloud (VPC), you can organize your resources into subnets. A subnet is a section of a VPC that can contain resources such as Amazon EC2 instances.
## Internet gateway
To allow public traffic from the internet to access your VPC, you attach an internet gateway to the VPC.
![Internet gateway](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/JtigqyfVR7iYoKsn1ee4sQ_69b244acd3f04813bc2c997b9d7d83cd_Internet_gateway.png?expiry=1665446400000&hmac=gjl7ZM9one20fAzQuAuXKa_vqoVFPYMxV22ZVujpsbE)

An internet gateway is a connection between a VPC and the internet. You can think of an internet gateway as being similar to a doorway that customers use to enter the coffee shop. Without an internet gateway, no one can access the resources within your VPC.

## Virtual private gateway
Here’s an example of how a virtual private gateway works. You can think of the internet as the road between your home and the coffee shop. Suppose that you are traveling on this road with a bodyguard to protect you. You are still using the same road as other customers, but with an extra layer of protection.The bodyguard is like a virtual private network (VPN) connection that encrypts (or protects) your internet traffic from all the other requests around it. 
![Virtual private gateway](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/m7JWN_MlRBWyVjfzJfQV2w_d5d7e759f59c44ff891fe9d062603fe7_Virtual-Private-Gateway.png?expiry=1665446400000&hmac=D--chFxyKTsE1jzOpXBX08Ff3yd2TpxxzkLT0UbYnLE)

A virtual private gateway enables you to establish a virtual private network (VPN) connection between your VPC and a private network, such as an on-premises data center or internal corporate network. A virtual private gateway allows traffic into the VPC only if it is coming from an approved network.

## AWS Direct Connect
AWS Direct Connect is a service that enables you to establish a dedicated private connection between your data center and a VPC.  
Suppose that there is an apartment building with a hallway directly linking the building to the coffee shop. Only the residents of the apartment building can travel through this hallway. 
This private hallway provides the same type of dedicated connection as AWS Direct Connect. Residents are able to get into the coffee shop without needing to use the public road shared with other customers. 
![AWS Direct Connect](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/h3jOQrMiSDy4zkKzIog8ew_efdbade19174425b85b6566bbb6579da_AWS-Direct-Connect.png?expiry=1665446400000&hmac=ci--XVxXJalhJQ4XP5c0O4nIElLim5waXO6T2Jc1Un0)

# [Subnets and Network Access Control Lists](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/MXgJu/subnets-and-network-access-control-lists)
A subnet is a section of a VPC in which you can group resources based on security or operational needs. Subnets can be public or private. 
![Subnet](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/IuYyEivXQXemMhIr17F3qg_3d5d4c825541434f8407e33d7048d9e3_Subnets3.png?expiry=1665446400000&hmac=ut6EJhaWkUa4fjazj0UQjDCw5OX2Z92bU3600gvRiAc)

Public subnets contain resources that need to be accessible by the public, such as an online store’s website.

Private subnets contain resources that should be accessible only through your private network, such as a database that contains customers’ personal information and order histories. 

## Network Traffic in a VPC
When a customer requests data from an application hosted in the AWS Cloud, this request is sent as a packet. A packet is a unit of data sent over the internet or a network. 
It enters into a VPC through an internet gateway. Before a packet can enter into a subnet or exit from a subnet, it checks for permissions. These permissions indicate who sent the packet and how the packet is trying to communicate with the resources in a subnet.
The VPC component that checks packet permissions for subnets is a network access control list (ACL).
## Network Access Control Lists (ACLs)
A network access control list (ACL) is a virtual firewall that controls inbound and outbound traffic at the subnet level.
For example, step outside of the coffee shop and imagine that you are in an airport. In the airport, travelers are trying to enter into a different country. You can think of the travelers as packets and the passport control officer as a network ACL. The passport control officer checks travelers’ credentials when they are both entering and exiting out of the country. If a traveler is on an approved list, they are able to get through. However, if they are not on the approved list or are explicitly on a list of banned travelers, they cannot come in.
![ACLs](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/zalo09JzRtSpaNPSc3bUzg_1a33ef5c42294d678b633f023cad0357_ACLs.png?expiry=1665446400000&hmac=aHAUW2hBqG4UMfXsj2awv9W7peUNWup_Jcsj_9YHycg)

By default, your account’s default network ACL allows all inbound and outbound traffic, but you can modify it by adding your own rules. For custom network ACLs, all inbound and outbound traffic is denied until you add rules to specify which traffic to allow. Additionally, all network ACLs have an explicit deny rule. This rule ensures that if a packet doesn’t match any of the other rules on the list, the packet is denied. 

## Stateless Packet Filtering
Network ACLs perform stateless packet filtering. They remember nothing and check packets that cross the subnet border each way: inbound and outbound. 
Recall the previous example of a traveler who wants to enter into a different country. This is similar to sending a request out from an Amazon EC2 instance and to the internet.
When a packet response for that request comes back to the subnet, the network ACL does not remember your previous request. The network ACL checks the packet response against its list of rules to determine whether to allow or deny.
![Stateless Packet Filtering](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/IT1vh3SMRZG9b4d0jEWRpw_c64f09027a6a4e75b868128e6838ed81_stateless.png?expiry=1665446400000&hmac=bCNeWjs_OmMg3HvYEhTedYeXZIcqLDZCmWWUGNuuy6k)

After a packet has entered a subnet, it must have its permissions evaluated for resources within the subnet, such as Amazon EC2 instances. 

## Security Groups
A security group is a virtual firewall that controls inbound and outbound traffic for an Amazon EC2 instance.
![Security Groups](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/MXgJu/subnets-and-network-access-control-lists)

By default, a security group denies all inbound traffic and allows all outbound traffic. You can add custom rules to configure which traffic to allow or deny.
For this example, suppose that you are in an apartment building with a door attendant who greets guests in the lobby. You can think of the guests as packets and the door attendant as a security group. As guests arrive, the door attendant checks a list to ensure they can enter the building. However, the door attendant does not check the list again when guests are exiting the building

## Stateful Packet Filtering
Security groups perform stateful packet filtering. They remember previous decisions made for incoming packets.
Consider the same example of sending a request out from an Amazon EC2 instance to the internet. 
When a packet response for that request returns to the instance, the security group remembers your previous request. The security group allows the response to proceed, regardless of inbound security group rules.
![Stateful Packet Filtering](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/HSQHiuCoR3WkB4rgqJd1pA_a832a55bf8b24f358ac0a2e7c2504239_Stateful.png?expiry=1665446400000&hmac=nB872YViDyF9-VyzSYk0NdBa_L11WqBiGRou1M-D5Ik)

Both network ACLs and security groups enable you to configure custom rules for the traffic in your VPC. As you continue to learn more about AWS security and networking, make sure to understand the differences between network ACLs and security groups.

![network ACLs](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/ULa-zH4MTHq2vsx-DPx6xg_75ffd32fc93b4897812bb144d3a51176_stateful2.png?expiry=1665446400000&hmac=3ZOTIoEuKASs8qXUjorfBaCGthkuHEi3h99Eeiw2W2c)

# [Global Networking](https://www.coursera.org/learn/aws-cloud-practitioner-essentials/supplement/Y32MM/global-networking)
## Domain Name System (DNS)
Suppose that AnyCompany has a website hosted in the AWS Cloud. Customers enter the web address into their browser, and they are able to access the website. This happens because of Domain Name System (DNS) resolution. DNS resolution involves a DNS server communicating with a web server.
You can think of DNS as being the phone book of the internet. DNS resolution is the process of translating a domain name to an IP address. 

![DNS](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/nIVOzpcgQnqFTs6XIAJ6kw_40390dcbe8cc4598a9c77dba6aacb862_global-networking.png?expiry=1665446400000&hmac=9RCIm5l0WNZMFyhVQCSWno0IgGKgH4h7wk0rKHA9gsA)

For example, suppose that you want to visit AnyCompany’s website. 
1) When you enter the domain name into your browser, this request is sent to a DNS server. 
2) The DNS server asks the web server for the IP address that corresponds to AnyCompany’s website.
3) The web server responds by providing the IP address for AnyCompany’s website, 192.0.2.0.

## Amazon Route 53
Amazon Route 53 is a DNS web service. It gives developers and businesses a reliable way to route end users to internet applications hosted in AWS. 
Amazon Route 53 connects user requests to infrastructure running in AWS (such as Amazon EC2 instances and load balancers). It can route users to infrastructure outside of AWS.
![ Amazon Route 53 and Amazon CloudFront deliver content](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/_U7EaNoSQuqOxGjaEhLqeg_303dd3fef2024ca1b8036096537913ff_global-networking2.png?expiry=1665446400000&hmac=m2HifK3fwiOutqdACnvZoeYiaTHjSxR2TE0ooqO7Eqg)
