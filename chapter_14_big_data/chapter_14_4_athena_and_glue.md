# Chapter 14.4 Amazon Athena and AWS Glue

What is Athena?
- interactive query service that makes it easy to analyze data in S3 using SQL
- query data without having to load it into a database

What is Glue?
- serverless data integration service that makes it easy to discover, prepare and combine data
- perform ETL workloads without having to manage underlying servers 

Using them Together
- put Glue Crawlers on s3 bucket to structure data and query it with Athena

Exam Tips
- Athena is the serverless SQL service
	- only tool that allows you to query S3
- Athena and Glue are serverless
- Glue is serverless ETL
- they work together very well
- Glue can help you design a schema
