# Chapter 18.3 Caching Your Data with ElastiCache and DAX

What is ElastiCache?
- managed version of two open source technologies
- Memcached and Redis
- avoid common issues rolling it out yourself

Memcached vs Redis
- both site in front of your database
- Memcached
	- just a database caching solution
	- not a database, not failover no multi AZ no backup
- Redis
	- caching solution
	- can function as a standalone database
	- NoSQL database
	- has fail-over and multi AZ support
	- supports backups

DynamoDB Accelerator (DAX)
- in-memory caching solution
- reduces database response times from milliseconds to microseconds
- lives inside a VPC, highly available
- you are in control of nodes, sizes, maintenance windows, etc

ElasitCache vs DAX
- DAX is only for DynamoDB
- ElastiCache is more flexible
	- sits in front of RDS or if using Redis, can be a database solution on its own

Exam Tips
- choose answers with database caches
- Redis is a cache and non-relational database
- DAX is for DynamoDB
- sits in front of database
- internal caching solutions
