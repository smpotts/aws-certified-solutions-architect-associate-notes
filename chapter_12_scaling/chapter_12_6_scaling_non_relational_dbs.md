# Chapter 12.6 Scaling Non-Relational Databases

Scaling Options (in DynamoDB)
- scaling is simplified when using DynamoDB
- provisioned model : set how many reads and writes you need
	- can set up autoscaling min, max and target utilization (70% 
of read or write capacity)
	- good for predictable workloads
	- most effective scaling model
- on-demand : sporadic workload
	-  AWS handles scaling and management you just pay a bit more

Demo
- DynamoDB -> create table
- Customize settings -> Read/ write capacity settings
	- on-demand : AWS handles everything
- read and write capacity listed as on demand
- can go back and change to the provisioned model
- can auto scale read and write capacity separately
	- set the min max and target utilization for each one
	- use CloudWatch to monitor what your history is so you choose the right values for min and max
- have to keep it as provisioned for 24 hours 

Exam Tips
- cost is a big factor scaling in DynamoDB
- predictable work load : provisioned capacity
- unpredictable : on-demand
- need to know the access patterns to decide
- on-demand is more expensive
- design for the database matters, avoid keys with similar values
- can switch between provisioned and on-demand but can only change once every 24 hours

