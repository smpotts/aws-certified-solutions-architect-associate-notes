# Chapter 14.6 Moving Transformed Data Using AWS Data Pipeline

AWS Data Pipeline Definition
- ETL service for automating movement and transfer of our data

AWS Data Pipeline Overview
- define data driven workflows and automate them
- define your parameters, enforces your chosen logic
- highly available, distributed, fault tolerant infrastructure
- automatically retries failed activities
- can send SNS notifications
- works with logs of different storage services : RDS, Redshift, S3
- works with compute services like EC2 and EMR 

Components to Know
- pipeline definition : specifies business logic aspect
- managed compute : service will create things like EC2 instances to perform activities
- task runners : poll for different tasks and perform them when they are found
- data nodes : define the locations and types of data that will be input and output
- activities : pipeline components that define the work to perform

Popular Use Cases
- processing data in EMR using Hadoop streaming
- importing or exporting DynamoDB data
- copying CSV files or data between S3 buckets
- exporting RDS data to S3
- can set scheduled triggers
- copying data to Redshift

Example Diagram
- task runners authenticate to the database
- export data from RDS to S3 using the task runners
- once it's in S3
- generate reports in EMR
- set schedules for specific tasks

Exam Tips
- Data Pipeline is a managed ETL tool
- data driven service
- can create dependencies between tasks and activities
- automates the movements and transformations of your data
- has many storage integrations
- integrates with compute services
- integrates with SNS to notify on success/ failure
- managed ETL services, automatic retries, data driven workflows -> AWS Data Pipeline
