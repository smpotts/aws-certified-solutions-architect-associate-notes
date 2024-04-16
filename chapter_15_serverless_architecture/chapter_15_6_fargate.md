# Chapter 15.6 Removing Servers with Fargate

What is Fargate?
- serverless compute engine for containers
- still use ECS or EKS without managing servers
- requires that you run ECS or EKS

EC2 vs Fargate
- EC2
	- EC2 pricing model, it's a better deal,
	- if you are running it constantly
	- you have to deal with underlying OS
- Fargate
	- don't have to deal with OS
	- pay based on resources allocated
	- short running tasks
	- isolated environments

How Does Lambda Compare?
- select Fargate when you have more consistent workloads
- Fargate allows Docker use across the organization and a greater level of control by devs
	- more consistent workloads
- Lambda is harder to standardize
	- good for a small single function
	- quickly respond to an event and shut down
	- has a time window limit

Console Demo
- create task definition choose Fargate
- have to define CPU and memory for Fargate
- want things to finish in the least amount of time with least amount of resources
- create cluster

Exam Tips
- Lambda : lightweight functions, run quickly, event driven things, something fast
- Fargate : containers that don't need to run all the time
- EC2 : containers need to run all the time and really concerned about costs
- Fargate is serverless, requires EKS or ECS
- EC2 when long-running content and costs / Fargate for temporary
- Fargate for containers and things that need to run longer / Lambda for short running things
