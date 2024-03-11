# What Is Amazon Aurora?

What is Aurora?
- Amazon's database they created themselves
- it's a mysql, postgres compatible database engine

Aurora Performance
- 5x better performance than mysql and x3 better than mysql
- at a much lower price point

Basics
- auto scales
- 2 copies of the data are contained in each AZ with a minimum of 3 so you have 6 copies

Scaling
- transparently handles the loss of up to 2 copies of data without affecting database write availabilty and up to 3 copies
- storage is self healing

Types of Aurora Replicas
1. aurora replicas : 15 read replicas
	- automated failover enabled
2. mysql replicas : up to 5 replicas
3. postgres replicas : 

Backups
- automated backups always enabled
- don't effect perforamnce, neither do snapshots
- can share snapshots with other accounts

Aurora Serverless
- on demand auto scaling configuration
- serverless db cluster that automatically starts, shuts down and scales automatically
- spikey workloads
- simple, cost effecitve for unpredictable workloads

Exam Tips
- 2 copies of data in each AZ, min of 3 so 6 copies
- can share snapshots
- 3 types of replicas
- automated failover only for Aurora
- automated backups by default
- aurora serverless for cost effective, infrequent, intermittent workloads
