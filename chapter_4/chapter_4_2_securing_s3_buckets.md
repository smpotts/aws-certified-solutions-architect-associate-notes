# Chapter 4.2 Securing Your Bucket Using S3 Block Public Access

Object ACLs vs Bucket Policies
- object ACLs work on an individual object level
- bucket policies work on the entire bucket level

Demo
- s3 is a global namespace
- buckets can be deployed into particular regions
- http 200 if upload is successful
- to make an object public
	- click permissions on the bucket so that not all objects are blocked from public access
	- object ownership -> ACLs enabled
	- click on an object -> Make public using obj ACL
	- verify by clicking on the object url
- do not make things public on an individual object level

Exam Tips
- buckets are private by default
- have to allow public access on bucket and objs to make them public
- object ACLs to make individual objects public
- bucket policies to make the entire bucket public
- http 200 status code when upload is successful