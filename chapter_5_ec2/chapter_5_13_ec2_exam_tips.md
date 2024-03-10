# EC2 Exam Tips

EC2 Overview
- EC2 is like a VM
- hosted in AWS
- pay for what you use

Pricing Options
- on demand: pay by second or hour, flexible, no contract
- spot: unused capacity at a discount, prices fluxuate
- reserved: 1-3 years, more upfront more savings, known or fixed requirements
- dedicated: a physical ec2 server dedicated for your use

AWS Command line interface
- give uses least privilege
- create iam groups and assign users to groups
- group perms via policies and users inherit permissions
- secret access key: only see once, if you lose it you can regenerate it, will have to re-configure
- don't share key pairs
- supports linux, windows and mac

Roles
- the preferred options
- don't hardcode with roles
- policies control a roles permissions
- updates: you can update them
- you can attach and detach

Security Groups
- changes take effect immediately
- you can have any # of instances in a SG
- you can have multiple SGs on an instance
- inbound traffic blocked by default
- all outbound traffic is allowed

Bootstrap Scripts
- script that runs when instance first runs
- runs at root level
- passes user data to the ec2 instance

Comparing user data and metadata
- user data is bootstrap scripts
- meta data is data about ec2 instance

Networking with EC2
- ENI: basic networking, low cost
- EN: reliable and high throughput
- EFA: high performance computing, ML, OS-bypass

Placement Groups
- cluster placement: low latency, high trhoughput
- spread placement: critical instances on diff hardware
- partition placment: mulitple ec2 instances, HDFS, HBase, and Cassandra
- cluster can't span multiple AZs
- only certain types of instances can be used in plavements groups
- can't merge placements groups
- homogeneous instances
- can move existing one into group

Dedicated Hosts
- licenses and compliances
- physical instance dedicated to your use

Spot Instances and Fleets
- can block from terminating with spot block
- spot fleet is collection of instances

VMware
- can deploy vCenter using VMware
- extending private VMware Cloud to the AWS public cloud

Outposts
- extending AWS to your data center
- bringing AWS to you
- racks: large deployments
- servers: smaller deployments

vCenter on AWS allows you to extend your private cloud to the AWS cloud.
