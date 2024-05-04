# Chapter 16.13 Advanced IAM Policy Documents

Amazon Resource Names (ARNs)
- uniquely identify a resource in AWS
- follow the same syntax
- Amazon is split into multiple partitions
- format -> arn:partition:service:region:account_id:resource
- :: means there is an omitted value

IAM Policies
- JSON documents that define permissions
- identity policy
- resource policy
- not effect until attached
- list of statements
- policy document is a list of statements
- each statement matches an AWS API request
- effect is allow or deny
- matched based on their action
- resource is based on what the action is against

Permission Boundaries
- used to delegate administration to other users
- prevent privilege escalation or unnecessarily broad permissions
- control max permissions an IAM policy can grant

Exam Tips
- if you don't explicitly allow something, it is implicitly denied
- explicit denies trump everything else
- only attached policies have an effect
- AWS joins all applicable policies
- there are AWS managed policies and you can create customer managed policies