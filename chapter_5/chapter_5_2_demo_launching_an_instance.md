Demo: Launching an EC2 Instance

Demo
- Launch Instance
- Choose and Amazon machine instance -> default
- Instance type
	- t2 is general apps, t2 micro is the smallest
- VPC: virtual data center in the cloud
- subnet: different availability zones
- leave basically everything as default
- Add storage
	- use default, 8 GB EBS volume
- Create new security group
	- ssh, http and http permissions
	- CIDR address ranges: who can access these modes
		- 0.0.0.0 means anyone
- security key: key to administrate the linux server, allows you to get into your EC2 instance
	- create a new key pair
	- download the key pair
- launch instance

How to access instance
- Connect
- EC2 instance connect
- an aws terminal window opens
- elevate to root: sudo su
- yum update -yes
