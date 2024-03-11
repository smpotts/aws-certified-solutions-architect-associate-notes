# Chapter 3.3 Permanent IAM Credentials

The Building Blocks
Users: physical person
Groups: put users into groups by job functions
Roles: internal usage within AWS, allows one part of AWS to access another part of AWS

Best practices
- for users to inherit permissions from groups
- apply an IAM policy document to a group
- never share user accounts, a user = one physical person

Principle of Least Privilege
- only assign a user the minimum amount of privileges they need to do their job

Demo
- programmatic access generates access key and secret key
- AWS has prepopulated policies for job functions
- can define password policy
- identity provider, can set up SSO if you setup trust
- active directory federation can allow users to login to AWS with an SSO password

Exam Tips
- IAM is global
- root account created when first setup account, do not use day to day, secure it
- new users have no permissions when first created
- access key id and secret keys are used for programmatic access
	- only get to view them once
- always set up password rotation
- IAM federation: combine existing user accounts with AWS
	- uses SAML as standard which is active directory
