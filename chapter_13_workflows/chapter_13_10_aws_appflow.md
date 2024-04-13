# Chapter 13.10 Ingesting Data from SaaS Applications to AWS with Amazon AppFlow

What is AppFlow?
- fully managed service
- securely exchange data between SaaS and AWS services
- like Salesforce to S3
- ingest data from 3rd party data venders and put it into AWS
- bidirectional service, but not all all supported

Important Terms and Concepts
- flow : what transfers data between source and destination
- data mapping : how data from the source is placed in the destination
- filters : control which data records are transfered into the destination
- trigger : how the flow runs 

Example Diagram
- create source and destination connection
- map fields
- create filters
- run the flow using a trigger

AppFlow Use Cases
- transferring Salesforce records into AWS Redshift
- use it for ingesting and analyzing Slack conversations into s3
- migrating of Zendesk of Helpdesk support tickets
- transfer aggregate data on a scheduled basis to s3

Exam Tips
- AppFlow : fully managed integration service for transferring data to and from SaaS service
- bi-directional but make sure it's supported
- needing an easy and fast transfer of SaaS or 3rd party data into AWS -> think AppFlow!
