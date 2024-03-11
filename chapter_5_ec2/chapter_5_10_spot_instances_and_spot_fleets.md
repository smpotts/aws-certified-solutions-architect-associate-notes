# Timing Workloads with Spot Instances and Spot Fleets

spot instance: take advantage of unused ec2 capacity, 90% discount

when they should be used: stateless, fault tolerant, flexible applications
- big data, containerized workloads, ci/cd, high performance computing

Spot Prices
- decide on max spot price, instance provisioned as long as the spot price is below your maximum spot price
- hourly spot price varies depending on the capacity and region
- if spot price > max you have 2 minutes to decide if you want to stop them and resume later or terminate the instance

Spot Blocks
- you can use a spot block to stop your spot instance from being terminated even if the price goes above your max
- 1- 6 hours

Pricing History
 - you can get your spot instance pricing history
- breaks down by region
- great flexibiility if you do pricing research

Use Cases
- big data
- image and media rendering
- high performance computing
- ci/cd

Where they are NOT useful
- persistent workloads
- critical jobs
- databases

Terminating Spot Instances
Request type: one-time or persistent
- if one-time, when the price > max then the instance is terminated
- if persistent, looks to see if the request is open, active or disabled
- if you have an open and persistent spot request you can't just terminate the instance, it will keep provisioning
- have to cancel spot request

Scenario Based Question: how do you go in and terminate spot instance under a persistent spot request?
- Go in and cancel the spot request
- Then terminate the instances

Spot Fleets
- collection of spot instances and optionally on demand instances
- attempts to launch all the instances to meet the request
- request is fulfilled if there is capacity and your max price > current price
- tries to match target capacity within the price constraints
- you can define launch pools
- define operating systems, availability zones, instance types
- you can have multiple pools and the fleet will choose the best way to implement
- it will stop launching instances once the prices or threshold is met

Strategies
- capacityOptimized: optimal capacity for the number of instances launched
- diversified: spot instance distributed across all pools
- lowestPrice: instances come from a pool with the lowest price, this is the default
- intancePoolToUseCount: instances are distributed across the number of spot instances you specify

Exam Tips
- spot instances save up to 90%
- when you don't need persistent storage
- can use a spot block to stop instances from terminating
- a spot fleet is a collection of spot instances
	- can configure with the different strategies
