# Chapter 12.7 High Availability and Scaling Exam Tips

4 Questions to ask yourself re: availability and scaling
- is it highly available? (always choose high availability)
- which is appropriate: horizontal or vertical scaling?
	- generally favor horizontal but not always
- is the solution cost-effective?
- would switching databases fix the problem?
	- can do this easily in AWS
	- relational -> non-relational

Auto Scaling
- autoscaling groups are only for EC2 instances
	- other services might have a build in solution
- want to pick solutions that get ahead of the workload, favor solutions that are predictive rather than reactive
- bake AMIs to reduce build times : avoid long provisioning times to put everything in an AMI
	- this is better than using user data
- spread out : put things in multiple AZs
- steady state groups : allow us to create a solution where the failure of a legacy resource that can't be scaled where we can't have more than 1 online
- ELBs are essential : for health checking instances and distributing traffic

Databases
- RDS has the most db scaling options
- horizontal scaling usually preferred
- read replicas
- DynamoDB scaling : comes down to access patterns

