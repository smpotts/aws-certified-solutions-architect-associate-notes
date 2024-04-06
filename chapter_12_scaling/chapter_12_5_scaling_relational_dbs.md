# Chapter 12.5 Scaling Relational Databases

4 Ways to Scale
- vertical scaling : resizing from one size to another to create greater performance
	- easiest and first step
- scaling storage : storage can be resized, but only able to scale up not down
	- Aurora automatically scales database in 10 gb increments
- read replicas : creating read copies can help spread out the workload
- relational databases + read heavy workloads = read replicas
- Aurora serverless : shifts burden to aws, unpredictable, and using Aurora 

Demo
- Modify database instance class
- Aurora scales database storage in 10 GB increments
- This will cause downtime 

Exam Tips
- don't shy away from switching relational database to non-relational database
- read replicas : when we have read heaby workloads
	- have to update code because you get separate endpoints
- scale storage up only
- veritcal scaling if your instance to start is insufficient
- multi AZ should always be turned on
- pick Aurora whenever possible for relational databases, favored over the others