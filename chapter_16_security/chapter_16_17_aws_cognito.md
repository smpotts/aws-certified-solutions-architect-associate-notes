# Chapter 16.17 Authenticating Access with Amazon Cognito

** 2-3 questions on Cognito on the exam

What is Cognito?
- authentication, authorization and user management for web and mobile apps
- authentication engine
- users can sign in with FB, Google, Amazon, Apple etc.

Features
- signup and sign in options for apps
- access for guest users
- identity broker between app and web id providers
- syncs user data across multiple devices
- recommended for all mobile applications that call AWS services

Use Cases
- authentication
- 3rd party authentication
- access sercer side resources
- access AWS AppSync resources

User Pools and Identity Pools
- user pools : directories of users that provide sign up and sign in options
- identity pools : allow you to give your users access to other AWS services
- can use them separately or together

How It Works Broadly
...

Cognito Sequence
1. authenticate and get tokens : device to user pool
2. exchange tokens and get AWS credentials
3. access AWS services using credentials

Exam Tips
- user pool : user directory that provides signup and signin options
- identity pool : allows users to access other AWS services
- can be used together or separate
- seq of events : 
	- 1. device authenticates and gets a token
	- 2. token sent to an identity pool
	- 3. identity pool gives you AWS credentials and using those you can access AWS services
