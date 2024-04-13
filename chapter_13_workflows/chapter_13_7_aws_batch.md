# Chapter 13.7 Executing Batch Workloads Using AWS Batch

AWS Batch Service Overview
- helps run batch computing workloads in the cloud
- workloads run on EC2 or ECS/ Fargate
- makes things simpler : removing heavy lifting for maintenance and configuration
- automatically provisions and scales
- no installation required

Important Components
- job : unit of work that gets submitted
- job definition : specifies how the job is to be run
- job queue : job submitted to the queue until it is scheduled to be run
- compute environment : compute resources used to run your jobs

Fargate or EC2 Compute Environments
- AWS recommends that you use Fargate for most batch jobs
- EC2 best choice when you need a custom API, vCPU requirements, memory requirements
	- or if you need a GPU or Graviton CPU
	- large number of jobs : dispatched at a higher rate

AWS Batch or AWS Lambda
- time limits : Lambda has 15 minute execution time limit
- disk space : Lambda has limited disk space
- runtime limitations : Lambda has limited run times, more custom should use Batch
- Batch uses Docker
- choice depends on your use case

Managed or Unmanaged Compute Environments
- Managed : AWS manages compute and instances types
	- compute resources defined when env is created
	- EC2 intanves are launched into VPC subnets
	- default is the most recent and approved AWS ECS AMI
	- can use your own AMI
	- leverage Fargate, Fargate spot or Spot instances
- Unmanaged : manage everything for yourself entirely
	- less commonly used
	- good choice if you have really complex or specific requirements

Exam Tips
- long running workloads : long running event driven workloads
- anything running for more than 15 minutes
- managed service
- jobs : units of work
- job definitions : blueprints within the jobs
- all jobs submitted to queues
- Batch vs Lambda : Lambda has runtime, execution time and storage size limitations
- what types of compute : # jobs, resource requirements
- managed : leverage AWS for capacity and compute
- unmanaged : you manage EVERYTHING


