# Chapter 15.10 Orchestrating Containers Outside AWS Using Amazon EKS Anywhere and Amazon ECS Anywhere

EKS Anywhere Overview
- a way to run on-prem EKS
- based on the EKS Distro : allows for deployment, usage and management methods for clusters in your data center
- offers full lifecycle management of multiple K8s clusters
- operates independently of AWS services

EKS Anywhere Concepts
- control plane : operated completely by the customer
- location : entirely within customer data center or ops center
- updates : done by manual CLI or Flux
- curated packages: extend core functionalities
	- only on Enterprise Subscriptions

ECS Anywhere Overview
- management of container apps on-prem
- no orchestration needed : operational efficiency
- completely managed : enables standardization of container management
- no ELB support
- added external launch type for external instances

ECS Anywhere Requirements
- must have SSM Agent, ECS Agent and Docker installed
- must first register external instance as SSM Managed Instances
- easily create an installation script
	- contains SSM activation key and commands for required software
- execute scripts on prem or on bare metal services
- deploy containers using the EXTERNAL launch type

ECS Anywhere Example Diagram
...

Exam Tips
- EKS anywhere
	- not commonly used or featured on the exam
	- based on EKS-D which allows you to run EKS on prem
	- allows users to maintain similar operational efficiency
	- all managed by you
- ECS anywhere
	- feature within ECS
	- allows for AWS managed container orchestration on prem
	- reqs : SSM Agent, ECS agent and Docker installed
	- register and deploy : execute scripts containing required steps and use the EXTERNAL launch type
