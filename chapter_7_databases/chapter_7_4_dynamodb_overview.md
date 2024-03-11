# DynamoDB Overview

What is DynamoDB?
- Amazon proprietary database
- noSQL database
- document and key value data models

High Level DynamoDB
- stored on SSD storage
- in 3 data centers
- eventual consistent reads, can opt into strongly consistent reads

Eventual consistent reads vs strongly consistent reads
- eventually means that consistency usually reached within a second
- strongly means you don't have to wait

DynamoDB Accelerator (DAX)
- fully managed, highly available, in mem cache
- 10x performance improvements
- reduces request time significantly
- DAX handles the cache between the app and DynamoDB, app only talks to DAX

On-Demand Capacity
- pay per request
- balance cost and performance
- no min cost

Security
- encryption with KMS
- site to site VPN
- direct connect
- works with IAM policies and roles
- cloudwatch and cloud trail
- vpc endpoints

Exam Tips
- stored on ssd storage
- in 3 data centers
- eventual consistent reads : consistency within one second, strongly consistent immediately