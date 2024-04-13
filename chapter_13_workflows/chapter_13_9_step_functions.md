# Chapter 13.9 Coordinating Distributed Apps with AWS Step Functions

AWS Step Functions Overview
- serverless orchestration service
- graphical console
- made of state machines and tasks
- state machine : a workflow
- task : a specific state within the workflow
- state : a single step within a workflow

Executions
- step functions have two workflows : standard and express

Workflows
- executions are instances where you run your workflows in order to perform your tasks
- standards : exactly-once execution
	- can run for up to one year
	- long running workloads that need to have an auditable history
	- up to 2,000 executions per second
	- pricing based on state transition
- express : at least one execution
	- can run up to 5 minutes
	- useful for high event rate workloads
	- IoT data
	- pricing based on executions, duration and memory consumed

States and State Machines
- states are flexible
- leverage states to make decisions based on input
- use a specific language ASL Amazon States Language
- states are elements within your state machines
- ex: online pickup order : each step of the process is a state

Integrated AWS Services
- Lambda
- Batch
- DynamoDB
- ECS / Fargate
- SNS
- SQS
- API Gateway
- EventBridge

Different States
- pass : passes any input directly to its output - no work done
- task : single of unit that gets performed (Lambda, Batch)
- choice : adds branching logic to the state machine
- wait : chooses a delay
- succeed : stops execution successfully
- fail : stops executions and marks them as failures
- parallel : run parallel executions
- map : runs a set of steps based on an input array

Exam Tips
- step functions : severless orchestration service for event driven task executions
- standard workflows for long running auditable executions
- express executions for high event rate executions
- everything written in Amazon States Language format
- states : elements within state machines where things happen w/in workflow
- there are MANY integrations
- know the state types 
- if you have to add a wait period think of step functions
