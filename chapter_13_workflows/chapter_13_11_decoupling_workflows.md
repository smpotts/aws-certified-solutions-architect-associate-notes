# Chapter 13.11 Decoupling Workflows Exam Tips

Ask yourself:
- are the workloads synchronous or asynchronous?
- what type of decoupling makes sense?
- does the order of messages matter?
- what type of application load will we see?


What to know for the exam
- SQS : can duplicate messages, 
	- queues are not bi-directional
	- know the defaults
	- messages last up to 14 days
	- if ordering is important you need to pick FIFO queues
- SNS : email, text, pushed based notification
	- used with CloudWatch alarms
- API Gateway : acts as a secure front door for external comms for things coming into our environment
- AWS Batch : long running, batched workloads ( > 15 minutes)
	- things that need batch workload queues 
	- on demand alternative to Lambda (runtime reqs or execution timeouts)
- AWS MQ : managed message broker, RabbitMQ or ActiveMQ
	- specific messaging protocols : JMS, STOMP, AMPQ
- Step functions : serverless orchestration service
	- different workflow decision requirements
	- condition checks, failure catches or long wait period
- AppFlow : 3rd party SaaS data ingestion into AWS
	- bi-directional

