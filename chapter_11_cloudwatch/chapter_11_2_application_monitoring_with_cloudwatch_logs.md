# Application Monitoring with CloudWatch Logs

What is CloudWatch Logs?
- a tool that allows us to monitor, store and access log files from a variety of sources
- allows you to query for potential issues or relevant data

3 CloudWatch Log Terms
- log event: a data point, contains the data and a timestamp
- log stream: collection of log events from a single source (like single instance)
- log group: collection of log streams, web server logs across all hosts together, care about the collective

Features
- filter patterns: look for specific terms/ errors in the logs
- CloudWatch Logs Insights: allows you to use SQL like commands to query logs and look for general trends
- alarms: alert on the trends and patterns you have identified

Demo
- install CloudWatch agent
- install CloudWatch logs on ec2 instance
- have to give permissions for a resource to write to CloudWatch logs

Exam Tips
- logs go to CloudWatch logs. if we don't need to process them and JUST store them, then we can think about s3
- go to tool unless explicitly calls for real-time solution
- can create alarms based on metrics and filter patterns
- could watch must be installed and configured 
- SQL like querying -> CloudWatch Logs Insights
