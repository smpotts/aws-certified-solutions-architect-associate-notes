# Chapter 15.14 Serverless Architecture Exam Tips

Lambda
- loves roles
- be familiar with triggers : s3 events, Kinesis, EventBridge
- has runtime (15 m) and RAM limitations
- any AWS API call can be made

Containers and Images
- open source : Kubernetes
	- managed solution : consider AWS EKS and EKS Anywehere
- Fragate cannot work along it needs ECS or EKS
- containers are flexible
- know about the Docker file, image, upload to a repo
- ECR : container image storage repo

Aurora Serverless
- on demand auto scaling database
- perfect usage for variable traffic and workloads
- great for capacity planning

X-Ray
- gain app insights using requests and responses of services at different points in the app flow
- integrates with API Gateway and Lambda

AppSync
- managed GraphQL interface
