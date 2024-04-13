# Chapter 13.1 Decoupling Workflows Overview

Tight Coupling
- if something goes wrong the whole chain is broken
- one instance talking directly to another EC2 instance
- simple but leads to a lot of problems

Loose Coupling
- instead want to have load balancers that routes traffic to a group of EC2 instances
- better than tightly coupling in almost all situations
- scalable, highly available, managed service 

What's Coming Up
- SQS : simple queue service, messaging tool that can decouple applications, could replace the load balancer
- SNS : simple notification service, push out notifications
- API Gateway : put a safe scalable, highly available front door to the application

Exam Tips
- never tightly couple applications
- never want an EC2 instance talking to another EC2 instance
- always loosely couple at every level
- no one single way to decouple applications