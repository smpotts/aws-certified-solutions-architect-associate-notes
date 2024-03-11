# Chapter 6.9 EBS Exam Tips

EBS: SSD Volumes
- highly available and scalable storage volumes that you can attach to ec2
- general purpose gp2 ssd: suitable for boot disks and general apps
- gp3: the new one
- io1 provisioned iops: latency sensitive apps, OLTP, more expensive
- io2: the new one, best durability

EBS: HHD Volumes
- throughput optimized hdd st1: cannot be a boot volume, suitable for etl, data warehouse
- cold hdd sc1: less frequently accessed data, cannot be a boot volume, lowest cost

Tips for Volumes and Snapshots
- volumes exist on ebs and volumes exist on s3
- snapshots are point in time pictures of volumes and are incremental
- first one is slow
- you can share snapshots between accounts
- you can change type or resize

AMIs EBS vs Instance Store
- instance store are ephemeral storage
- can reboot both
- instance store volumes cannot be stopped
	- can stop ebs
- both root volumes deleted on termination
	- can save the ebs 
- AMI is a blueprint for an EC2 instance

Encrypted Volumes
- data at rest, in flight, snapshots, created from snapshots are encrypted
- encrypt unencrypted by creating a snapshot, encrypting and creating an AMI from the snapshot

EC2 Hibernation
- preserves the in memory RAM
- faster to boot up
- don't need to reload OS
- only for certain instance types
- cannot be hibernated more than 60 days

EFS
- can support thousands of connections
- only pay for what you use
- data stored across multiple AZs
- highly scalable shared storage using NFS -> EFS

FXs Overview
- EFS: highly distributed for Linux
- FSx: centralized storage for Windows apps
- FSx Lustre: high speed, high capacity storage, high performance computing, can store data on s3

Storage Options Use Cases
- s3: serverless obj storage
- glacier: archive objects
- efs: centralized storage across multiple availability zones
- fsx lustre: high performance Windows
- ebs: persistent storage for ec2 instance
- ephemeral storage for ec2 instance
- fsx for windows: file storage for windows instances

AWS Backup
- used for consolidations to backup different AWS services
- use with organizations
- centralized control, compliance
