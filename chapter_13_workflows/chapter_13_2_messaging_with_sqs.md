# Chapter 13.2 Messaging with SQS

Poll-Based Messaging
- have a producer of messages that writes message into SQS queue and then backend consumer can read messages

What is SQS?
- messaging queue that allows asynchronous processing of work
- one resource writes a message and another retrieves the message
- doesn't have to immediately respond if it's not ready to receive that content
- not direct communication the queue is a buffer

Important Settings
- delivery delay : default is 0 but can be set up to 15 minutes, delaying the notification being sent (showing up in the queue)
- message size : up to 256 KB of text in any format
- encryption : messages are encrypted in transit, but you can add encryption at rest
- message retention : by default messages only live for 4 days, can be set between 1 and 14 days 
- long vs short polling : short polling is the default but we should set long polling
- API calls to SQS are not free
- long polling : connect and then wait a little bit (more cost-effective), focus on answers on the exam that pick long polling
- queue depth : can be a trigger for autoscaling EC2 instances
- vital to know defaults and what happens when you changes the settings

Visibility Timeout
- message is locked for 30 seconds
- settings you can configure
- remains in the queue but no other instances can see it
- if it doesn't get processed in 30 seconds the messages goes back in the queue
- if it gets processed the queue deletes this message

Exam Tips
- SQS is featured heavily on the exam
- be able to explain every single setting
- messages live up to 14 days
- long vs short polling : long polling is more efficient
- 256 KB of text in any format