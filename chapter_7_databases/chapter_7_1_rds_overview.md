# Relational Database Service (RDS) Overview

Relational Databases
- tables: traditional spreadsheet
- rows: the data items
- columns: fields in the database 

RDS Engines
- sql server
- postgresql
- maria db
- mysql
- oracle
- amazon aurora

RDS Advantages
- up and running in minutes
- basically an ec2 instance but you don't have access to the OS, only database
- multiple AZs, primary in one and secondary in another
- automated failover built in
- automated backups

When to use RDS?
- used for OLTP

OLTP vs OLAP
- OLTP: processess data from transactions in real time
	- comes and goes quickly
- OLAP: analytics processing
	- process complex queries to analyze historical data
	- data analysis

**Data warehouses are not for OLTP databases

Multi-AZ
- creates an exact copy of your production data in another availabilty zone
- AWS handles the replication for you
- Aurora is always multi-AZ, others can be configured to be
- for disaster recovery
- cannot run queries on the standby when the primary is active
- it is not for performance improvements

Unplanned Failures and Maintenance
- if we have a failure, Amazon will keep the same web address and failover to the secondary, all automated

Demo
- production template will make it multi AZ and create a standby instance
- endpoint is a dns address
- modify -> Availability and Durability and make it multi AZ

Exam Tips
- RDS database types
- RDS is for OLTP not OLAP
