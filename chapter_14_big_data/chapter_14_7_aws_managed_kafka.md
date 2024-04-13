# Chapter 14.7 Implementing Amazon Managed Streaming for Apache Kafka (Amazon MSK)

Amazon MSK Overview
- streaming service used for Apache Kafka
- fully managed service
- provides you control plane operations
- leverage the data plane operations so you can focus on producing and consuming data
- great for existing applications and plugins leveraging Kafka

Important Components and Concepts
- broker node : specify # of broker nodes per AZ
- zookeeper nodes : created for you
- producers, consumers and topics : Kafka data pipeline operations allow you to create topics and produce/ consume data
- flexible cluster operations : it will do this for you

Resiliency in Amazon MSK
- automatic detection and recovery from failure scenarios
- detects broker failures and works on mitigation or replacement
- reduces data
- impact time limited to complete detection and recovery
- after recover, communicate with the same broker IP address as before

Good to Know
- MSK Serverless : cluster type that offers serverless cluster management
	- provisions and scales for you
	- fully compatible with Kafka
- MSK Connect : allows devs to stream data to and from Kafka

Security and Logging
- integrates with KMS for server-side encryption
- encrypts data at rest by default
- TLS 1.2 for encryption in transit between brokers
- deliver broker logs to S3, CloudWatch, Kinesis Firehose
- metrics are gathered and sent to CloudWatch
- logs to CloudTrail

Exam Tips
- fully managed service for Apache Kafka
- handles control plane operations : creating, updating and deletion of clusters
- you work on the data plane operations
- automtic recoveries : detects and mitigates common failures
- integrates with KMS
- allows for logging
- think MSK when you see stuff about Kafka

