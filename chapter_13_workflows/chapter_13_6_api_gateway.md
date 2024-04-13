# Chapter 13.6 Fronting Applications with API Gateway

What is API Gateway?
- fully managed service
- safe "front door" on your application
- allows you to publish, monitor, maintain API
- put restrictions on how resources can be consumed

Notable Features
- security : protect architecture with WAF to protect endpoints (security group on steroids)
- prevent abuse : DDoS protection, rate limiting
- ease of use

API Gateway in Practice
- API Gateway handles nonstatic content on the A Cloud Guru site

Console Demo
- API Gateway has native integration with Lambda
- offers different stages for test, dev, prod etc.
- useful to front applications that we are hosting in AWS

Exam Tips
- just need to know the use cases
- APIs are the front door to your application
- anytime it is talking about an API, if it's a custom built application you should be using API Gateway
- API that you are building or managing yourself
- can help in a DDoS attack since you can use WAF
- can create different versions of APIs
- allows you to stop baking credentials into your application

