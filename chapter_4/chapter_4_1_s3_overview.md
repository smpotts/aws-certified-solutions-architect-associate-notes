# Chapter 4.1 S3 Overview

What is S3?
- S3: object storage in the cloud
- store and retriever any amount of data
- scalable
- cannot run an OS or database on it
- images, text, web pages, videos
- safe place to store files
- data spread across multuple devices and facilities to ensure durability and availability
- built for availability 
	- 99.95-99.99% service availability
- designed for 11 9's durability for data stored in S3, so should not lose any objects

Basics
- unlimited storage
- objects up to 5 TB in size
- store files in buckets

Working with Buckets
- universal namespace
- when you create bucket, the bucket name is:	https://bucket-name.s3.us-east-1.amazonaws.com/ralphie.jpg
- when you upload, if it is successful you will receive an HTTP 200 code

Key-Value Store
- key: name of the object
- value: data itself
- version id: when enabled
- metadata: data about the data stored i.e. content-type or last_modified date

S3 Standard
- default
- highly availability and durable
- 11 9's durability
- desgined for frequently accessed data
- suitable for most workloads

Characteristics
- Tiered storage: different storage classes
- Lifecycle management: rules to transition objects to a cheaper storage tier
- Versioning

Securing Data
- server side encryption: encrypt things stored in the bucket
- access control lists: which accounts or groups are granted access
- bucket policies: what actions are allowed or denied for that bucket

Data Consistency
- strong read after write consistency 
-  after you write objects you can immediately list

Exam Tips
- s3 is obj based storage for flat or static files
- up to 5 TB
- unlimited storage
- universal name space
- files stored in buckets
- urls are built the same way
- successful uploads generate a HTTP 200 status code
- S3 Obj Tips
	- key: obj name
	- value: data
	- version id
	- metadata
