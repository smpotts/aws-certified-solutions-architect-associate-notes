# Chapter 4.4 Versioning Objects in S3

What is versioning?
- can have multiple versions of an obj within a bucket

Advantages
- all versions of obj stored in s3
- backup tool
- can't get rid of it all you can do is suspend it
- integrates with lifecycle rules
- supports MFA: need to protect objs from being accidentally deleted by enabling MFA

Demo
- Properties -> bucket versioning -> enable bucket versioning
- list versions toggle top right
- previous versions will give access denied even if you have a policy that enables all objs to be public, it does not apply to previous versions
	- you can go and make them public though
- if you delete with versioning, it puts a delete marker on the object
	- restore an object by deleting the delete marker

Exam Tips
- all versions are stored in s3, all writes and even deletes
- good backup tool
- once setup it can't be removed on suspended
- can be integrated with lifecycle rules
- supports MFA