# Chapter 14.9 Big Data Exam Tips

4 Questions to ask
- what kind of database works?
- how much data do we have?
- is serverless a requirement?
- how do we optimize costs?

Redshift and EMR
- Redshift is not a replacement for RDS
- Redshift only supports single AZ deployments
	- can create separate clusters is different AZs
- EMR is made up of EC2 instances

Kinesis, Athena, Glue
- only service with reali-time response
- SQS and Kinesis can act as queues
- Kinesis is faster and can store data for up to one year
- serverless SQL querying is Athena
- Glue is serverless ETL that will help create a schema for your data

QuickSight and OpenSearch
- QuickSight does not analyze the data just visualize it
- OpenSearch is primarily used for analyzing log files and various docs especially in an ETL process
- OpenSearch used to be Elasticsearch

Data Pipeline
- meant to created automated workflows for movement and transformation of data
- managed ETL tool
- integrates with storage services
- data driven and task dependent ETL workloads are the perfect use case

MSK
- building and running Apache Kafka streaming applications
- service handles control plane ops like creating, updating and deletion
- you manage data plane ops
- push broker logs to s3, CloudWatch
- integrates with CloudTrail


