# Using NAT Gateways for Internet Access

What is a NAT Gateway?
- network address translation
- can use NAT Gateways to allow instances in a private subnet to connect to the internet or another service
- prevents the internet from initiating a connection with those instances
- put a NAT gateway in the public subnet
	- same AZ as public subnet
	- private subnet can use it to get internet access

Route table for the private subnet does not have a connection out to the internet

We provision the NAT Gateway in the public subnet

NAT Gateway Facts
- redundant inside the availability zone
- starts at 5 Gbps and scales to 45 Gbps
- no need to patch
- not associated with security groups
- automatically assigned a public IP address

Demo
- in VPC section -> NAT Gateways
- put in the public subnet
- allocate elastic IP address
- need to go into route tables and make a route out to the internet
- add a route
	- destination is open 0.0.0.0/0
	- target is NAT gateway to give a route out to the internet
	- from main table to the NAT gateway
- can now go in and do installations

Exam Tips
- NAT gatways are redundant
- no need to update or patch
- not associated with a security group
- given a public IP address