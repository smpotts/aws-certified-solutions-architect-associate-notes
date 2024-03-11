# Increasing Read Performance with Read Replicas

What is a Read Replica?
- a ready-only copy of the primary database
- you aren't putting more load on the main database
- great for read heavy workloads
- multi AZ for disaster recovery, read replica for boosting performance (can be in another AZ, can be cross region)
- each read replica has it's own DNS endpoint
- can be promoted to become their own databases
	- this breaks the replication

Key Facts
- scaling read performance
- requires automatic backups
- multiple read replicas are supported, up to 5 each instance

Demo
- RDS -> new instance
- Actions -> Create read replica
- can choose multiple AZs
- can choose the region or specific AZ
- whether or not public access
- the replica will have a Role that is "Replica"
- to promote:
	- Actions -> Promote read replica
- can go in and make the read replica multi AZ

Exam Tips
- multi AZ vs read replica
	- multi AZ is exact copy in another AZ
	- disaster recovery
	- read replica is a read only copy used to increase performance and can be in multiple AZs
		- great for heavy read loads