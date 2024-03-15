# Monitoring Exam Tips

Are yourself:
- What is the best tool to monitor with?
- Is that metric available by default?
- Where can I find those logs?
- Do I need to adjust my alarm threshold?

CloudWatch Overview
- main tool for anything alarm related
- not everything should go through CloudWatch
- know your intervals: standard metrics every 5 mins, detailed every minute

Application Monitoring with CloudWatch Logs
- services can integrate with CloudWatch like EC2, RDS, on prem
- SQL? think CloudWatch Logs Insights
- real time means Kinesis
- CloudWatch is not for real time

Visualizing and Monitoring Containers
- Grafana for visualizing container metrics
- monitoring container metrics at scale -> Prometheus
- both managed services