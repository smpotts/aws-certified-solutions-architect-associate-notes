# Networking with EC2

Different Virtual Networking Options
- you can attach 3 different types of virtual networking cards to your ec2 instances
1. (ENI) Elastic Network Interface: for basic day to day networking
2. (EN) Enhanced Networking: uses single root I/O virtualization, high performance networking
3. (EFA) Elastic Fabric Adapter: accelerates high performance computing and ML

Common ENI Use Cases
- create a management network
- dual homed instances with workloads/ roles on distinct subnets
- use network and security appliances in your VPC
- create a low budge, highly availably solution
- when you create an ec2 instance it will have an ENI in it by default

Enhanced Networking (EN)
- higher IO performance and lower CPU utilization
- comes in 2 flavors

ENA vs VF (a part of enhanced networking)
- Elastic Network Adapter (ENA): supports network speeds up to 100- Gbps
- Intel 82599 Virtual Function Interface (VF): only supports network speeds up to 0 Gbps, typically used on older instances
- always want to be using the elastic network adapter over VF

Elastic Fabric Adapter (EFA)
- device that you can attach to ec2 instance to accelerate high performance computing and machine learning
- provides lower and more consistent latency and higher throughput than the TCP transport traditionally used in cloud based HPC systems
- high performance computing
- OS ByPass : make it a lot faster and with much lower latency
	- only supported with latency

Exam Tips
- just need to know the 3 types of network adapters and when to use them
- ENI: basic
- EN: faster speeds, reliable, high throughput
- EFA: high performance computing, ML, OS-bypass