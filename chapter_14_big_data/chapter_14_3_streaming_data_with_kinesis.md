# Chapter 14.3 Streaming Data with Kinsesis

What is Kinesis?
- allows you to ingest, process and analyze real-time streaming data

Kinesis Data Streams
- real time streaming for ingesting data
- real time
- you are responsible for creating the customer and scaling the stream

Data Streams Architecture
- producer
- Kinesis data stream (with shards)
- consumers
- put the data in a database, S3, somewhere else

Kinesis Data Firehose
- data transfer tool to get information to S3, Redshift, Elasticsearch
- near real time
- plug and play AWS architecture
- handles the scaling
- way simpler

Kinesis Data Analytics and SQL
- you can analyze data using standard SQL
- no servers
- only pay for the amount of resources you use as data passes through

Kinesis vs. SQS
- Kinesis when you need real time 
- both can handle messages and data but only Kinesis can do it in real time

Exam Tips
- real time -> Kinesis Data Streams
- near real time ->  Kinesis Firehose
- transforms data : Kinesis Data Analytics
- automatically scales your streaming service : Data Firehose
