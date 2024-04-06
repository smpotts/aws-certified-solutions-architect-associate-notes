# Chapter 12.3 Scaling EC2 Instances with Auto Scaling

Auto Scaling Groups
- collection of EC2 instances treated as one cohesive unit as far as scaling and management goes

Auto Scaling Steps
- define your template first to tell group all the settings it needs to know
- define networking space (this is why we don't put this in template) the auto scaling group defines this
- cost : define whether to use spot instances or on demand or reserved instances
- ELB :  sits in front of autoscaling group
	- can use the health check of the load balancer
	- will deregister host and spin up a new instance
- set scaling policies : define min max and desired capacity
- notifications : SNS

Auto Scaling Restrictions
- minimum : lowest # of instances that the group will ever have online ( at least 2 for high availability)
- maximum : highest # of instances that we want in the group
- desired : how many instances do we want right now (at this very second) 

Demo
- EC2 -> Autoscaling Group
- choose template
- can mix and match on demand and spot instances
- pick VPC and subnet(s)
- can attach a load balancer
- can enable ELB health check if we are using the load balancer
- set min and max capacity (desired between min and max)
- says we have 0 instances? autoscaling will create 2 in the pending state
- terminates when we don't need that many anymore

Exam Tips
- ensure we are creating autoscaling group across multiple AZs
- ensure you are spreading resources
- networking defined in autoscaling group : want to use multiple subnets in multiple AZs
- remember ELB : will use the ELB health check
- limits : min max and desire govern rules
- autoscaling group can notify when things are coming online or coming down
- auto scaling groups will balance instances across all AZs

