# Demo: Provisioning a VPC - Part 1

Chapter 8.2 Part 1
- Go to VPC
- You can see VPC in all regions
- Launch VPC wizard doesn't create from scratch
- Your VPCs

Default VPC
- already has a route table and a network ACLs associated with it
- click into VPC, route table, subnets

Subnets
- every subnet correlates to one availability zone
- subnets cannot span multiple AZs

Create VPC
- VPC only
- CIDR address range: manual input
- recommends 10.0.0.0/XX XX has to be between 16 and 28
- no IPv6
- tenancy: Default
- create!

Creating a new VPC creates 3 things by default:
1. security group
2. main route table
3. main network ACL

Security Groups
- creates a new one

Route Table
- no subnets associated with it

Need to create new subnets
- subnets are virtual firewalls
- can be public/ internet accessible or private

Create subnet
- choose an AZ
- name it CIDR address range - AZ
- available IPv4 addresses: 251
	- these are 5 missing because they are reserved for AWS for router, network address, IP address of DNS server, reserved for future and network broadcast address
	- always lose 5 IP addresses

 Exam Tips
- VPC logical data center
- consists of different components
- one subnet anchored to one availability zone
