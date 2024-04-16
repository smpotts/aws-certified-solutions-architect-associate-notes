# Chapter 16.7 Monitoring S3 Buckets with Macie

What is Macie?
- automated analysis of data
- uses ML and pattern matching to discover sensitive data stored in s3
- alerts you if you have unencrypted buckets and public buckets
- buckets shared with AWS accounts that are outside of organization
- great for GDPR and HIPAA

Personally Identifiable Information (PII)
- personal data used to establish an individuals identity
- can be used in identity theft and fraud
- email addresses, addresses, SSN, drivers license number, etc.

Automated Analysis of Data
...

Macie Alerts
- you can filter and search Macie alerts
- can integrate with EventBridge and Security Hub and other services like Step Functions to automatically take action

Exam Tips
- Macie is an automated way of discovering PII using AI
- look for PII, PHI and financial data
- good for preventing identity theft
- sent alerts via EventBridge
- integrate with other AWS services like Step Functions