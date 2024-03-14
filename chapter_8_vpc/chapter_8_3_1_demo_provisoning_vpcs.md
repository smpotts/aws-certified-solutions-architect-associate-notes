# Demo: Provisioning a VPC - Part 1

Chapter 8.3 Part 2

Subnets
- auto-assign public IPv4 addresses
	- default ones are yes
	- manually created ones are no
- edit subnet settings
	- enable auto assign IPv4 addresses (for the public one)
- now we need to make it internet accessible and for that we need internet gateways

Internet Gateways
- already one in there
- create new one
- state is detached
- attach it to VPC
	- only one per VPC
- now we need a route out to the internet

Route tables
- click on the one 
- subnet associations 
	- the public and private ones we created
- create a new route table for public subnet
- give it our VPC
- all public subnets go with this one
- Main is No
- now we need a route out to the internet
- Edit routes
- add a route and point to internet gateway
- everytime we provision a new subnet it will be provisioned to main route table but doesn't have a route out to the internet
- want to go into subnet associations and add the subnet we created that is public
- public subnet will no longer be associated with the main route table
- want to put EC2 instances in subnets

EC2
- create a new one as a web server
- put it in the VPC and public subnet
- auto assign public IP
- can confirm private IP address is within the range we expected

RDS
- create a database instance
- put it in the VPC
- put it in the private subnet
- add to security group

SSH into EC2
- copy the ec2 instance public IP address and ssh into it
- sudo yum update confirms it has access to the internet

Want to put the DB in a new Security Group
- create a new security group
- put in the VPC
- create inbound and outbound rules
- can look it down but we want every server in public subnet to be able to talk to the DB
- move the database into the new security group

Grab the private IP address, no public IP address
- ping the address
- create a private key
- change perms then ssh into the ec2 instance with the key
- does not have a route out to the internet from the private subnet so you cannot do any updates