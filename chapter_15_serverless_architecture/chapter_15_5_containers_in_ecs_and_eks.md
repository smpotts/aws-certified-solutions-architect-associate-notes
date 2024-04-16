# Chapter 15.5 Running Containers in ECS or EKS

Problems with Containers
- handling a fleet of containers

Why ECS?
- can help us as applications grow
- manage N number of containers
- integrates with load balancers
- integrate with roles to talk to other services
- ease of use

Using Kubernetes
- open source container management and orchastration platform
- can be used on-prem and in AWS
- EKS is Amazon's managed service

ECS vs EKS
- ECS focuses on ease of use
	- doesn't work on prem
- EKS has some additional workarounds that you have to do for cloud compatibility
- focus on ECS when all cloud, EKS when you need a little outside AWS 

Console Demo
- create a task definition
- define memory and CPU
- add container
- create cluster
- launch task
- open IP address

Exam Tips
- ECS is preferred method
- exception is when scenario needs on prem access then EKS
- open source : EKS
