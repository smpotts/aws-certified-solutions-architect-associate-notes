# ELB Overview

What is Elastic Load Balancing?
- automatically distributes traffic across multiple targets
- balances the load of web servers
- across multiple AZs

Types of Load Balancers
1. application load balancer: best for load balancing for http and https traffic, intelligent load balancing
2. network load balancer: extreme performance, think Lambo
3. classic load balancer: legacy, test, dev etc.

Health Checks
- all AWS load balancers can be configured with health checks
- sends request to load balancers instances to check their status
- healthy ones are in service, unhealthy ones are out of service
- on all registered instances
- load balancer only routes to healthy instances, will resume when it is restored

Exam Tips
- remember 3 ELB types: application = intelligent, network = extreme performance, classic = test/dev/legacy
- health check: route traffic to your instances or targets that are healthy