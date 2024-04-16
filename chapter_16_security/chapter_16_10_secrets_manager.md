# Chapter 16.10 Storing Your Secrets in Secrets Manager

What is Secrets Manager?
- service that stores, encrypts and rotates database credentials and other secrets
- automatically rotates credentials
- can apply find grained permissions
- programmatic retrieval
- reduces risk of compromised credentials

What You Can Store in Secrets Manager
- RDS credentials
- non-RDS credentials
- any other kind of secrets like API keys

Automatic Rotation
- if you enable rotation, Secrets Manager immediately rotates the secret once to test the configuration
- ensure all your apps that use credentials are updated to retrieve credentials using this service
- embedded credentials will break applications

Exam Tips
- Secrets Manager can use used to store applications secrets
- applications use the Secrets Manager API
- rotating credentials is super easy
- if enabled, Secrets Manager will rotate credentials immediately
- make sure all apps are configured to use Secrets Manager

