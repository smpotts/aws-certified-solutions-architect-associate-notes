# Chapter 4.6 Lifecycle Management with S3

What is lifecycle management?
- automates moving your objects between the different storage tiers to maximize cost effectiveness
- automating moving objects to save money

Lifecycle Management with Versioning
- can be used to move different versions to different storage tiers

Demo
- enable bucket versioning
- management -> lifecycle rules -> create
- apply to all objs in bucket
- use lifecycle rules actions to move certain objects
- create a set of rules for transitions
	- add different transition steps
- transitioning small objs to Glacier Flexible retrieval or Deep Archive will incur costs

Exam Tips
- lifecycle management rules automate moving objects between different storage tiers
- current and previous versions
