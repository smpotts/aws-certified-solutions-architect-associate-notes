# CloudWatch Overview

What is CloudWatch?
- monitoring and observability platform that gives insight into AWS architecture
- allows us to monitor multiple levels of our application and identify potential issues

CloudWatch Features
- system level metrics: is there a problem with a service, are we using it, does it have too many resources
- application metrics: get information to how the application is performing, what's happening inside the OS
- alarms: alerting on potential problems

Types of Metrics
1. default : things that AWS provides out of the box
- CPU utilization
- network throughput

2. custom : metrics that need to be provided by the CloudWatch agent installed on the host
- EC2 memory utilization
- EBS Storage Capacity
*AWS cannot actually see what is going on with memory unless you install a CloudWatch alert

Demo
- created and SNS topic and EC2 instance beforehand
- create alarm
- select metrics -> EC2
- in alarm
- send notification
- can trigger autoscaling or other actions
- can create an alarm to stop, terminate or reboot and instance
*need to know whether you have to have the agent installed

Exam Tips
- CloudWatch is the tool we use for monitoring
- know the basic checks you get by default
- have to create alarms yourself
- don't get extended checks out of the box
- the more managed a service is, the more checks you get out of the box
- standard reporting interval is every 5 minutes

** login to CloudWatch and look at the pre-installed metrics
- EC2, S3, RDS
