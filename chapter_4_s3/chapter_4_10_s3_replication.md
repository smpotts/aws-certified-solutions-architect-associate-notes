# Back up Data With S3 Replication

Used to be called cross region replication -> now just S3 Replication

S3 Replication
- way to replicate obj from obe bucket to another
- versioning must be enabled on both the source and destination buckets
- objects in an existing bucket are not replicated automatically
- delete markers are not replicated by default

Demo
- Create source bucket
- Leave everything as is for now
- Create destination bucket
- In the source bucket, upload object
- Management -> Create replication rule
	- Enable versioning
	- Enable, apply to all obj in bucket
	- Pick destination bucket
	- Enable versioning
	- Create an IAM role for replication
	- Can change destination storage class
	- delete markers are not replicated automatically but you can enable that
- After uploading a new file, it will replicate to the new bucket
- If you delete a file, since versioning is on, the deleted object and previous versions are still there
- Delete market will not be replicated in the target bucket

Exam Tips
- remember what replication is
- obj in existing bucket will not be replicated automatically
- delete markers are not replicated by default

