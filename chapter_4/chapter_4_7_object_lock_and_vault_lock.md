# Chapter 4.7 S3 Object Lock and Glacier Vault Lock

S3 Object Lock
** on the exam
- use it to store object using a WORM model: write once read many
- prevent objs from being deleted or modified
- meets regulatory requirements
- or protection against deletion

Governance Mode
- users cannot overwrite or delete unless you have special permissions
- permissions to alter the retention settings
- some users have to have settings

Compliance Mode
- protected obj version cannot be overwritten or deleted by ANY user
- retention mode and period cannot be changed

Retention Periods
- protects obj version for a fixed amount of time
- after retention period the obj version can be overwritten or deleted unless you also placed legal hold

Legal Hold
- s3 obj lock that allows you to place a legal hold on an obj version
- like a retention period it prevents the obj version from being overwritten or deleted
- can be freely placed and removed by user with permissions

Glacier Vault Lock
- allows you to deploy and enforce compliance controls with vault lock policy
- once locked it can no longer be changed

Exam Tips
- WORM -> S3 object lock
- obj lock can be done on objects or bucket
- governance mode and compliance mode
- compliance cannot be overwritten or deleted at all
- gov mode, some people can change
- WORM + Glacier -> Glacier vault lock
	- easy deploy and compliance controls
	- WORM model
	- once locked it can't be changed
