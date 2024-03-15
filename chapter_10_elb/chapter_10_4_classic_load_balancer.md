# Using the Classic Load Balancer

Classic Load Balancers
- legacy load balancers
- http and https
- layer 7 features
- strict layer 4 load balancing for apps that rely purely on TCP protocol

X-Forwarded-For
- when traffic is sent from a load balancer, the server access logs contain the IP address of the laod balancer only
- when EC2 instances logging, just getting internal IP address of the load balancer
- this is used to see which IP address it came from
*popular exam topic that comes up

Gateway Timeouts
- if app stops responding the classic load balancer responds with 504 error: running but cannot make a connection
- troubleshoot the web layer or database layer

Demo
- create a new classic load balancer in previous generation
- in default vpc
- internal: in a private subnet
- add listener and protocol
- configure health checks
- add EC2 instances
- status changes to in service
- copy DNS name of the load balancer and browse to it
- you will see it distribute across all the ec2 instances

Exam Tips
- 504 error means the gateway has timed out and you have to trouble the app or db
- if you need the IPv4 address of the end user you need to look for the x-forwarded-for header in the logs