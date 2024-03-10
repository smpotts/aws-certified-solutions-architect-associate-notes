# S3 Exam Tips

S3 Overview
- obj based storage
- not for OSs and databases
- files up to 5 TB
- unlimited storage
- files stored in buckets
- universal namespace
- bucket name in the URL
- https 200 upon successful upload

S3 Obj Tips
- key is the obj name
- value is the data itself
- version id : allows multiple
- metadata

Securing Buckets with S3
- private by default and so are objs
- object ACLs : on individual objects
- bucket policies : on entire bucket

Hosting a static website
- using bucket policies
	- make all objs public
- for static content
- automatic scaling

Versioning
- all versions stored in s3
- all writes saved
- deletes just put a delete marker on the obj
- can be a good backup tool
- can use with lifecycle rules to move old version
- supports MFA

Storage Tiers
- know them all and their use cases
- s3 standard: suitable for most workloads
- s3 IA: critical, long term, infrequently accessed
- s3 one zone IA: non critical
- s3 intelligent tiering: unknown or unpredictable access patterns

Lifecycle Management
- automates moving of objects between storage tiers
- can be used with versioning
- current and previous versions

S3 Object Lock and Glacier Vault Lock
- s3 object lock WORM model
- governance and compliance mode
- gov mode users cannot overwrite or delete without certain permissions
- compliance mode nobody can
- glacier vault lock allows you to enforce compliance controls such as WORM

Encryption
- ecncryption in transit: ssl/tls, http
- encryption at rest server side: sse-s3, sse-kms, sse-c
- client side encryption: do yourself before upload
- can enforce encryption with bucket policies

Optimizing S3 Performance
- adding prefixes to make performance better
- SSE-KMS has limitations, region specific
- upload and download counts towards quota
- can do multipart uploads and byte range fetches for downloads

Replication
- replicate obj from one bucket to another
	- used to do this across region but can do the same
- obj in existing buckets will not be replicated automatically
- delete markers not replicated automatically
