# Encrypting S3 Objects

Types of Encryption
**must understand this
1. encryption in transit
	- SSL/ TLS
	- HTTPS
2. encryption at rest: server side encryption
	- SSE-S3: server side encryption s3, s3 managed keys
		- AES 256 bit encryption
	- SSE-KMS: AWS key management service managed keys
	- SSE-C: customer managed keys
3. encryption at rest: client side encryption
- you encrypt files yourself and upload them

Enforcing server side encryption
- console
	- easiest way
- bucket policies
	- *sometimes comes up on exam

Enforcing server side encryption for s3 uploads
- upload is a PUT request and when enforcing encryption it adds encryption parameter
- you can create bucket policy that denies PUT requests that deny any requests that doesn't have the x-amz-server-side-encryption

Demo
- Creating new bucket
- Enable Default Encryption
	- Choose s3
- Upload some files
- Click on the object and you'll see it's encrypted
- with policies you can create a bucket policy to do the same

Exam Tips
- encryption in transit
	-ssl/ tls
	- https
- server side encryption
	- 3 kinds
- client side encryption: do it yourself before upload
- can enforce encryption using a bucket policy
