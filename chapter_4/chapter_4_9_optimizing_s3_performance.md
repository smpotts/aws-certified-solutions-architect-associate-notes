# Optimizing S3 Performance

S3 Prefixes
- just the folders inside the buckets

S3 Performance
- s3 has extremely low latency
- can also achieve a high number of PUT/COPY/POST/DELETE
- the more prefixes the higher performance you are going to get

If we wanted to get better performance out of S3:
1. spread our reads across different prefixes

More folders and subfolders the better performance we can get

Limitations with KMS
- there are built in limits with KMS
- uploading and downloading will count towards your KMS quota
- consider using native s3 encryption
- you cannot request a quota increase for kms

S3 Performance: Uploads
- multipart uploads
	- recommended for files over 10 MB
	- req for files over 5 GB
	- parallelized uploads -> increase efficiency

S3 Performance: Download
- s3 byte range fetches
	- parallelizes dowloads by specifying byte ranges
	- failue is only for certain byte ranges

Exam Tips
- remember what a prefix is: folders and subfolders
- more prefixes = better performance
- if you're using SSE-KMS there are built in limits
- uploading and downloading count towards KMS quote
- no quote increases
- use multipart uploads
- use s3 byte range fetches when downloading large files