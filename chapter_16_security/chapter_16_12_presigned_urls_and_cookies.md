# Chapter 16.12 Temporarily Sharing S3 Objects Using Presigned URLs or Cookies

Privacy
- all objects in S3 are private by default 
- obj owner can optionally share objects by creating a presigned URL
- grant time limited permission to download obj

Presigned URLs
- provide your security credentials, bucket name, object key, expiration date and time
- presigned urls are only valid for a duration of time

Access
- anyone who receives the presigned url can access the object
- presigned urls are a way to share something with someone in a bucket that is private

Presigned Cookie
- when you want to provide access to multiple restricted files
- cookie will be saved on the users computer and then they can browse all the contents

Console Demo
- create bucket
- add presign before the object name on the command line
- set expiration to expire

Exam Tips
- scenario where you need to share private files in your s3 buckets then use presigned urls 
- can set expiration date
