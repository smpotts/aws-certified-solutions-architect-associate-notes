# Chapter 16.11 Storing Your Secrets in Parameter Store

What is Parameter Store?
- capability of AWS Systems Manager which provides secure hierarchical storage for configuration data management and secrets management
- store data such as passwords, database strings, AMI IDs, license codes all as parameter values 
- plain text or encrypted

Costs
- free!

Limitations
- 10,000 max parameters you can store
- no rotation

Exam Tips
- parameter store when you are minimizing costs
- if you need +10,000 parameters, key rotation or the ability to generate passwords using CloudFormation then user Secrets Manager