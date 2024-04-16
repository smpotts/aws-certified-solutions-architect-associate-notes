# Chapter 16.2 Logging API Calls with CloudTrail

What is CloudTrail?
- increases visibility into user and resource activity in AWS
- CCTV monitoring
- tracking API calls who made them and when

Network Diagram
- when user does something
- all API calls are logged to an S3 bucket
- cannot log RDP or SSH traffic
- logs API calls made to AWS

CloudTrail Logging
- metadata around API calls
- identify of caller
- source IP of API call
- time of the API call
- request params
- response returned

Exam Tips
- after the fact incident investigation
- near real time intrusion detection
- industry and regulatory compliance
- logs all API calls made to your AWS account and stores logs in S3
