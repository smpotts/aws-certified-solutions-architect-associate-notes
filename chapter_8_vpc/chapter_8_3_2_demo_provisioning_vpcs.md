# Demo: Provisioning a VPC - Part 2

Demo
Public subnet
- edit subnet settings
- enable auto assign IPv4 addresses
- make it internet accessible with Internet Gateway

Create a new Internet Gateway
- give it a name
- need to attach it to VPC -> select VPC
- can only have one Internet Gateway per VPC

Route out to the internet
- via Route table
- by default the subnets will not be associated with any route tables

Main route table
- don't want main route table to have route out to the internet because every subsequent subnet will have a route out to the internet whether or not it is private

Create a new route table
- give it a name and vpc
- where we will put all our public subnets
- need a route out
- Edit Route
- Add a route
- point to the Internet Gateway
- when we provision new subnets they will be associated with the main route table, which does not have a way out to the internet

Add public subnet to the new internet facing Route table
- Edit subnet associations 
- Add public subnet
- public one will no longer be associated with the main route table

Put EC2 instances in private and public subnets
- database server in the private subnet
	- no public IP address
	- can ping the private IP address

Recap
- added a new Route table 
- new Network ACL
- New security group
- put instances in public and private subnet
- sshed from public to private subnet

