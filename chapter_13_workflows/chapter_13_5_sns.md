# Chapter 13.5 Delivering Messages with SNS

Push-Based Messaging
- have to be ready at any point in time to receive the message
- you don't get to grab it when you are ready

What is SNS?
- pushed-based messaging
- can be used to alert a system or a person
- proactively deliver messages to the endpoints subscribed to it

Important Settings
- subscribers : what is subscribed to the SNS topic, who will receive data from the topic
- message size : messages can be as large as 256 KB
- dead letter queue support
- FIFO or standard SNS
	- FIFO is not as useful, only supports SQS as a subscriber
- encryption
	- in transit by default
- access policies
- will not be featured quite as heavily on the exam as SQS

Console Demo
- create a standard topic
- retry is HTTP and HTTPS only
- create a subscription
- create 2 SQS queues
- with email you have to opt in
- have to have access policy appropriately setup or message will not make it from the SQS queue
	- SQS allow permissions for SNS to send to it

Exam Tips
- pushing/ alerts/ notifications = SNS
- push = SNS
- CloudWatch should be used to alert that something happened
- SES is based around marketing emails, email list, advertisers
- in general think SNS for email notifications
- no do overs
	- will only retry HTTP and HTTPS end points