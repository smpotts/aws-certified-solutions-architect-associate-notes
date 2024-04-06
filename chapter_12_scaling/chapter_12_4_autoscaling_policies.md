# Chapter 12.4 Diving Deeper into Auto Scaling Policies

Step Scaling
- puts instances in a warmup period when it gets close to a threshold

Instance Warm-Up and Cooldown
- warm up : stop instances from being places behind load balancer, failing health check and being terminated
- cooldown : pauses autoscaling for a set amount of time, helps to avoid runaway scaling events
- these help us avoid thrashing

Scaling Types
- reactive scaling : policy is responding to data points
- schedule scaling : if you have a predictable workload
- predictive scaling : AWS watching your application to combine reactive and schedule scaling looking at your historical data to create a model. Revisits it every 24 hours

Demo
- steady state autoscaling group : min max and desired capacity all set to 1
	- migrates between AZs between the subnets that are selected

Exam Tips
- scaling policies, min max and capacity important because you need to know what is cost effective
- scale out aggressively and then scale in conservatively
- put more in the AMI to make provisioning them easier
- use reserved instances to cover min count, spot instances if you can and then fail back to on demand
- CloudWatch #1 tool for telling it if it needs more or less