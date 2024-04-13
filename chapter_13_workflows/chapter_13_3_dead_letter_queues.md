# Chapter 13.3 Sidelining Messages with Dead-Letter Queues

Dead-Letter Queues
- just another SQS queue to temporarily sideline messages to
- can move problematic messages and not leave them in the queue forever

Demo
- create the dead letter queue
	- regular queue has to be created first
- 14 day maximum
- in the dead-letter queue, enable and then choose the arn of the queue to pull messages from
- create another queue
- max retry amount needs to be set to show how many tries before it is sidelined
- can send messages and interact with the queue from the console
- when the stopped the polling the message got pushed into the dead letter queue
- received count 2 : carries over, shows 2 tries

Exam Tips
- dead letter queues are the best and only sideline
	- move problematic messages and set them aside
	- same as the standard queues but just a place to hold onto the content
- want to set up CloudWatch alarm to look at queue depth
	- alarm for queue depth
- they are not special they are the same as standard SQS queue
- same retention window of 14 days
- can set up a SQS DLQ for SNS topics too
