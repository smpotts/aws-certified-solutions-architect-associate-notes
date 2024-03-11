# EFS Overview

What is EFS?
- elastic file system
- managed NFS that can be mounted on many EC2 instances at once
- can have centralized storage for ec2 instances in multuple AZs
- highly available and scalable but expensive
- web server farms, shared database
- shared storage across multiple instances

Use Cases 
- content management: word press blogs, share content between instances

Overview 
- linux based amis
- nfsv4 protocol
- encryption at rest
- file system that scales automatically
- pay per use

Performance
- 1000s of concurrent connections
- 10 Gbps throughput
- scales to petabytes

Controlling Performance
- can set what perforance you want
- gen purpose or max I/O

Storage Tiers
- can use lifecycle management
- standard and infrequently accessed

Demo
- create EFS
- EFS is regional : store data redundantly across multiple AZs
- automatic backups by default
- life cycle management enabled by default
- can set throughput

Exam Tips
- EFS: pay for what you use
- scales
- supports 1000s of connections
- multiple AZs
- highly scalable shared storages using NFS: network file system
