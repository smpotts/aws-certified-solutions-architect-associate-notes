# Chapter 15.12 Using AWS X-Ray for Application Insights

Service Overview
- service that collects data within your application about requests your applications serves
- view, filter and gain insights about requests and responses
- view calls to downstream AWS resources and other microservices/ APIs and databases
- traces : receives from applications to gain insights
- you can add tracing headers, send trace data or run the X-Ray daemon

AWS X-Ray Exam Concepts
- segment : data containing resource names, request details and other info
- subsegments : more granular timing and details information
- service graph : graphical representation of interacting services in requests
- traces : track paths of your requests
- tracing header : extra HTTP header containing sampling decisions and trace ID
	- X-Amzn-Trace-Id

AWS X-Ray Daemon
- software application that listens on UDP port 2000 to collect raw data and send it to AWS X-Ray API

AWS Integrations
- EC2 : install and run agent
- ECS
- Lambda : simple on and off toggle
- Elastic Beanstalk
- API Gateway
- SNS and SQS

Exam Tips
- application insights : X-Ray
- traces
- tracing headers
- segments
- integrates with a number of other AWS services
- things involving app requests, viewing response times of downstream systems and HTTP response analysis
