# Chapter 3.4 IAM Exam Tips

4 Steps to secure root account
1. MFA
2. create admin group for admins and assign permissions
3. create user accounts for admins
4. add users to the admin group

Policy documents
- used to assign permission
- JSON

Remember:
- IAM universal
- root account is created when you first setup, complete admin access, secure account and never log in day to day
- new users don't have permissions when first created

Permanent IAM Credentials
- programmatic access gives you access key and secret access key
	- not a username and password
	- only visible once
- always setup password rotation policies
- IAM federation : combine existing user accounts with active directory
	- SAML, basically AD