# Monitoring with Amazon Managed Service for Prometheus and Amazon Managed Grafana

What is Amazon Managed Grafana
- allows us to visualize data and query, correlate and visualize logs and traces

Amazon Managed Grafana Overview
- easy to deploy, operate and scale Grafana
- can create workspaces with dashboard visualizations and queries
- AWS manages the scaling, setup, and maintenance
- built-in security features like SSO
- pricing by active user per workspace
- integrates with several sources within AWS

Use Cases
- container metric visualization like EKS, ECS or Kubernetes
- IoT :data plugins 
- troubleshooting: centralizing dashboards and troubleshooting

What is Amazon Managed Service for Prometheus
- serverless Prometheus-compatibe service for securely monitoring container metrics at scale

Amazon Managed Service for Prometheus Overview
- open-source Prometheus data model and leveraging AWS scaling and availability
- automatic scaling
- designed for high availability
- choose your Kubernetes: EKS or self-managed
- PromQL : query language for exploring and extracting data
- data retention : stored in workspace for 150 days

Exam Tips
- Grafana: fully managed service for data visualization
- querying and correlating data
- Prometheus : serverless, monitoring container metrics at scale
- security and scaling
- can leverage VPC endpoints for secure VPC access
- Grafana has built in data sources
- Prometheus basically for Kubernetes
- Grafana used for container metric visualization : IoT, ECS, Kubernetes