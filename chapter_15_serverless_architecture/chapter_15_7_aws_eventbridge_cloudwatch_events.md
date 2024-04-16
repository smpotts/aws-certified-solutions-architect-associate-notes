# Chapter 15.7 Amazon EventBridge (CloudWatch Events)

What is EventBridge?
- CloudWatch events 2.0
- serverless event bus
- allows you to pass events from a source to an endpoint
- glue that holds serverless application together

Creating a Rule
- define a pattern : do you want the rule to be invoked by an events that happened
	- scheduled or based on an event happening
- select an event bus
	- AWS based events
	- custom events 
- select your target : what do you do when the event kicks off?
	- trigger a Lambda
	- post to an SQS queue?
	- send an email
- tag it

Console Demo
- AWS EventBridge
- create rule
- scheduled kickoff or an event pattern
- define the pattern
- choose service and event type
- in our example if EC2 stops, send an event
- you can choose certain instances
- AWS event bus
- select kick off a Lambda function
- tag it

Exam Tips
- EventBridge is the Glue that kicks off serverless architecture
- any API call that happens in AWS can kick off EventBridge which can trigger Lambda functions
- use EventBridge to kick off Lambdas
- EventBridge is the new name, but it used to be CloudWatch Events
- fastest way to respond to an API call
