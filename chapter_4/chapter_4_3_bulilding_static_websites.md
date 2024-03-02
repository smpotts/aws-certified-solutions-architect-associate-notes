# Chapter 4.3 Hosting a Static Website Using S3

Static Website Hosting
- s3 can be used for this
- dynamic websites, such as those that require database connections cannot be hosted on S3
- s3 scales automatically

Demo
- uncheck block public access
- properties -> static website hosting -> edit -> enable
	- specify the index document and error page
- now you have a url where you can visit the website
- add the html pages to the bucket
- make the bucket public
	- permissions -> edit bucket policy -> paste JSON

Exam Tips
- static website = s3
- bucket policies are used to make entire buckets public
- static content only
- automatic scaling with demand
