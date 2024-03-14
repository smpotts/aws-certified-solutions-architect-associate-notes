# VPC Overview

**one of the most difficult sections
**need to know how to build a VPC from memory

VPC Intro
- VPC: virtual data center in the cloud
- every region has a default VPC
- logically isolated part of the cloud where you can define your own network
- complete control over virtual network, own IP ranges, subnets, route tables, network gateways

Networking
- fully customizable network
- leverage multiple layers of security to help control access to EC2 instances and each subnet
- web tier : public facing subnet
- application tier : private subnet (talk to web and database tiers)
- databse tier : private subnet (can only talk to app tier)

VPNs
- virtual private network
- leverage the cloud as an extension of your data center

CIDR Address Ranges
- /16 more IP addresses than /24
- largest we can have is /16
- AWS reservers some IPs

Networking Diagram
- create VPC inside a region
- create VPC
	- choose IP address range /16 gives us the largest range of IP addresses
	- router
	- route table
	- network ACL
- public subset
- private subnet
- attach virtual private gateway
- add internet gateway to make it internet accessible
- Virtual Private gateway to be able to access private subnets

￼

What can we do with VPC?
- launch instances into it
- create custom IP addresses
- route tables
- internet gateway
- gives us more control and better security control

**you can block specific IP addresses using Network ACLs (NACLs) 

Default VPC vs Custom VPC
- default is user friendly, 
	- all subnets in default VPC have a route out to the internet, 
	- each EC2 instances has public and private address
- custom is fully customizable

Exam Tips
- think of VPC as logical data center
- consists of internet gateways, virtual private gateways, subnets, network ACLs, security groups
- one subnet is always in 1 AZ, cannot span multiple AZs
