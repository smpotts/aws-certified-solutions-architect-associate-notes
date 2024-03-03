# Security Groups and Bootstrap Scripts

Security Groups
- virtual firewalls for EC2 instance
- by default everything is blocked
- to let everything in 0.0.0.0/0
- in order to communicate via http/ssh you will have to open the correct ports

Bootstrap scripts
- a script that runs when the instance first runs
- automates the installation of applications

*do not need to know port numbers for the exam

Exam Tips
- changes to security groups take effect immediately
- you can have multiple security groups on an instance
- you can have multiple instances in a security group
- all inbound traffic is blocked by default
- all outbound traffic is allowed
- remember what a bootstrap script is
	- passes user data to the EC2 instance
	- can be used to install applications, do updates, etc