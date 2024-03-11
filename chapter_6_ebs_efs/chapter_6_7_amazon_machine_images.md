# Amazon Machine Images: EBS vs Instance Store

What is an AMI?
- Amazon machine image: provides information required to launch an instance
- you must specify an instance

5 Things You Can Base Your AMI On
- region
- OS
- architecture
- launch permissions
storage for your root device

EBS vs Instance Store
- whether the AMI is backed by EBS or Intsance store
- EBS: root device is an EBS volume created from an EBS snapshot
- Instance store: the root device is an instance store volume created from a template stored in S3

Instance store volumes
- "ephemeral storage"
- cannot be stopped
- not going to be saved if the instances is stopped
- if you delete the instance, you will lose the instance store volume 
- if the underlying host fails you will lose your data

EBS Volumes
- can be stopped
- can reboot and not lose your data
- will be deleted if the instance is terminated but it can be configured not to

Demo
- instance store cannot be stopped

Exam Tips
- remember the difference between instance store and EBS
- instance store volumes : data is ephemeral
-  if host fails the data is gone
- can reboot EBS and instance store volumes and not lose data
- by default root volumes will be deleted on termination
- an AMI is a blueprint for an EC2 instance