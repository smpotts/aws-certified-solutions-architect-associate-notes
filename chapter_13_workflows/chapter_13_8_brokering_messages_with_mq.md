# Chapter 13.8 Brokering Messages with Amazon MQ

Amazon MQ Overview
- managed message broker service
- easy to migrate existing apps
- multiple programming languages
- supports Apache MQ and Rabbit MQ
- easily leverage existing apps without managing or maintaining your own system

SNS with SQS vs Amazon MQ
- topics and queues
- 1-1 or 1-many messaging designs
- existing applications : if migrating existing apps with messaging systems in place
- new applications : look at SNS and SQS, simpler to use, more scalable
- publically accessible : MQ REQUIRES private networking
- SNS and SQS are publically accessible
- Amazon MQ has NO default AWS integrations

Configuring Brokers
- single instance broker: one broker in one AZ for development usually
	- RabbitMQ has a Network Load Balancer in front of it
- highly available: highly available, minimum downtime, architecture depends on broker engine type
- AmazonMQ for ActiveMQ : with active/ standby deployments
- AmazonMQ for RabbitMQ : groupings of 3 nodes behind load balancer

Exam Tips
- remember this is a managed broker service for easily migrating message broker systems into AWS
- supports Apache MQ and Rabbit MQ
- good for specific messaging protocols : JMS, STOMP, AMQP.., MQTT
- new or existing applications : new ones should try SNS with SQS
- restricts access to public networking
- single instance broker configurations
- highly available

