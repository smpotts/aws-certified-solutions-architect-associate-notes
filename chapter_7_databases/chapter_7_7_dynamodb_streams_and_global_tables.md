# Taking Your Data Global with DynamoDB Streams and Global Tables

Streams
- time order sequence of item level changes
- FIFO streams of data
- stored for 24 hours
- sequences broken up into shards
- inserts, updates and deletes
- combine with lambda functions for functionality like stored procedures

Global Tables
- managed multi master, multi region replication
- replication tables from one region to another
- good for globally distributed applications
- based on DynamoDB streams, need it turned on
- multi region redundancy
- build in to DynamoDB natively, can just turn it on
- replication latency under one second

Demo
- DynamoDB create table
- Partition key is unique key for table
- regional based service
- Explore table items: what's in the table
- click on table, Global Tables, create replica, choose region
- to undo, delete replica table

Exam Tips
- DynamoDB global tables gives to multi region replication
- based on DynamoDB streams
- good for globally distributed applications
- good for high availabilty and disaster recovery
- no application rewrites, just turn it on