# Chapter 15.8 Storing Custom Docker Images in Amazon Elastic Container Registry (Amazon ECR)

ECR Service Overview
- AWS managed container image registry
- ECR is a container registry service
- supports private repositories
- supports different formats

Components to Know
- registry : private registry is provided to each account, regional, create one or more for image storage
- authorization token : auth token required for pushing and pulling images to and from registries
- repository : contains all of your Docker images, OCI images and OCI artifacts
- repository policy: control all access to repos and images
- image : container image that gets push to and pulled from your repository

** Amazon ECR Public is a similra service for public image repositories for public repos

Features to Know
- lifecycle policies : helps management ofr images in your repos
	- test rules before you apply
	- rule cleanup
- image scaning : identifies software vulnerabilities
	- scan on push
	- retrieve results for the scans of each images 
- sharing : cross region support, cross account support
	- configured per repo and per region
- cache rules : caching public repos privately
	- ECR will periodically reach out to check current caching status
- tag mutibility : prevents tags from being overwritten
	- at the repo level

Integrations 
- will integrate with your own container infrastructure if you want
- ECS : can use the images in ECS
- EKS : can pull images for clusters
- Amazon Linux : containers can be used locally for your software development

Exam Tips
- container image storage service
- AWS managed
- supports Docker, OCI
- implement lifecycle policies
- leverage image scanning for security
- tag mutability
- managed container image registry, OCI, integration with EKS and ECS
