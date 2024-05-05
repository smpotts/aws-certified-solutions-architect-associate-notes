# Chapter 17.3 Elastic Beanstalk

What PaaS?
- platform as a service
- single stop application deployment model
- IT shop in a can : provision and manage all the infrastructure

What is Elastic Beanstalk?
- PaaS tool
- automation
- you control what it looks like : size of infra, where you want it to live
- deployments handled for us

Console Demo
- platform : most important step - support for different languages
	- can run a Docker container too but don't usually choose it
- Python, choose version
- sample application
- can pick AMI, security group, instance size, autoscaling group, roles, deployment, create a load balancer,
- env not part of VPC means it is using the default VPC
- shows recent events
- gives you a public url
- created a standard EC2 instance

Exam Tips
- not featured heavily on the exam, mostly high level
- one stop solution
- automate, speed, bring your own code
- is a PaaS : builds platform and puts app in it
- supports Windows and Linux and containerized applications
- good for simpler applications
- bigger apps outgrow it, long term not good
- not serverless
- it's creating and managing standard EC2 instances