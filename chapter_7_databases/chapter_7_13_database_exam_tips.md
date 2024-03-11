# Database Exam Tips

RDS
- RDS types: sql server, mysql, mariadb, Aurora, postgres, oracle
- oltp workloads
- not suitable for OLAP

RDS Multi AZ
- all updates and changes are applied to the secondary
- backups are taken from a secondary copy of the data
- automatic fail-over

Read Replicas
- scaling read performance not DR
- automatic backups must be turned on
- multiple read replicas supported
- disaster recovery

Multi AZ vs Read Replica
- multi AZ for disaster recovery, automatic failover
- read replica is a read only copy for better performance
- read replicas great for read heavy workloads

**You may use a read replica for disaster recovery of the source DB instance, either in the same AWS Region or in another Region

Aurora
- AWSs proprietary database
- always has 2 copies of data in a min of 3 AZs, 6 copies
- can share Aurora snapshots with other accounts
- 3 kinds of replicas: aurara, mysql, postgres
- automated backups by default
- can take snapshots and share them

Aurora Serverless
- cost effective option, relatively simple
- for infrequent, unpredictable, wokrloads
- serverless databases

DynamoDB
- stored on SSD
- spread across 3 data centers
- eventual consistent reads: consistency copies within second
- can change to strongly consistent reads: happens immediately

DynamoDB Transaction
- all or nothing operations
- financial transactions
- 2 options for reads
- 3 options for writes
- ACID requirements

DynamoDB On Demand Backups and Restore
- full backups at any time
- zero impact
- retained until deleted
- in same region as source table

DynamoDB Point In Time Recovery
- protects against accidental writes or deletes
- restore from any point in 35 days
- incremental backups
- not enabled by default
- last restorable rate 5 mins

DynamoDB Streams
- FIFO records of your data
- sequences broken into shards
- time ordered sequences
- stored for 24 hours
- can combine with lambda functions for functionality like stored procedures

Global Tables
- managed multi master multi region replication
- for apps globally distributed
- dynamodb streams must be enabled
- for disaster recovery or higher availability
- no app changes needed

Running Mongo in the Cloud
- AWS DocumentDB
- Move with Database Migration Service, deploy with DocumentDB

Cassandra
- migrating a cluster
- Keyspaces!

Neptune
- graph database
- often used as a distractor

QLDB
- also used as a distractor
- ledger database
- immutable, can only insert new records not update

Time Series Data
- Timestream
- temperature stations
- large amount of time series data
