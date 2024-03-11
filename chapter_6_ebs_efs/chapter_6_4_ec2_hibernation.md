# EC2 Hibernation

EBS Behaviors Reviewed
- we can stop and terminate instances
- if stopped the data is kept on the disk and will remain on the disk until the instance is started
- if the instance is terminated then the root device volume will also be terminated but we can save the volume if we want

When we start an EC2 instance:
- OS boots up
- user data script runs
- application starts

EC2 Hibernation
- OS is told to hibernate
- saves contents from RAM to EBS volume
- taking what's in RAM and saving down to disk

When you starten EC2 instance out of hibernation:
- EBS root volume is restored to it's previous state
- RAM contents are reloaded
- processes previously running are resumed
- previously attached data volumes are reattached and the instances retains it's instance id

In Action
- instance boots much faster since RAM/ state is preserved
- good for long running proceses 

Exam Tips
- hibernation preserves the in memory RAM to persistent storage
- makes resuming faster
- C M and R instance families
- cannot be hibernated for more than 60 days


