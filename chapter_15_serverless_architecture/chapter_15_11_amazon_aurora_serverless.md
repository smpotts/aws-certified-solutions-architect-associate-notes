# Chapter 15.11 Auto Scaling Databases On Demand with Amazon Aurora Serverless

Amazon Aurora Serverless Overview
- on-demand and auto scaling configuration for Aurora
- automation of monitoring workloads and adjusting capacity
- based on demand
- charged per-second
- budget friendly service

Aurora Serverless Concepts
- Aurora Capacity Units (ACUs) : measurement of how your cluster scales
- set a minimum and maximum of ACUs : for scaling requirements - can be 0
- allocated quickly by AWS-managed warm pools : compute shared between customers
- about 2 GiB of memory, matching CPU and networking capability
- 6 copies of data across 3 AZs
- multi AZ, highly available cluster

Use Cases
- variable workloads
- multi tenant apps 
- new applications and not sure what size db to use
- dev and testing of new features
- mixed use applications
- capacity planning : verify optimal capacity

Exam Tips
- on-demand, auto scaling, serverless version of Aurora
- capacity adjusted for you
- ACU : min and max for scaling needs
- billed per second for used resources
- variable workloads
- new apps not sure of sizing
- dev and testing needs
- same data resilience as the other service
- multi AZ


