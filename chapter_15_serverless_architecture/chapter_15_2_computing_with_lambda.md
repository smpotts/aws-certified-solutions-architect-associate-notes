# Chapter 15.2 Computing with Lambda

What is Lambda?
- serverless compute service that lets us run code without managing the underlying servers
- running code without computers

Building a Function
- requires that we pick from a list of supported runtimes : Java, Python, NodeJS
- can even run containers and run our own runtime
- permissions need to be attached
	- attach roles to Lambda functions
	- can make API calls with Lambda functions
- networking, can run on it's own or in a VPC
- resources : you get to define the amount of memory the function receives
- billed on resources and length the function runs
- something has to trigger the function

Console Demo
- create function
- author from scratch
- assign a role with appropriate permissions
- add trigger
- built in logging and monitoring with Lambda
- General configuration -> can set memory and timeout setttings

Exam Tips
- Lambda is used to add features and enforce things in AWS
- remove entries from a security group, start and stop instances
- good for microservices
- 10 Gigs of RAM and 15 minutes is longest it can run
- starts with triggers
- microservices
- easy to integrate, custom functions
- networking is optional