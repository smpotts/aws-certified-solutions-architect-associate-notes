# Protecting EBS Volumes with Encryption

EBS Encryption
- you can encrypt volumes with a data key
- you can manage the key yourself or AWS manage
- data at rest is encrypted
- snapshots encrupted
- all data moving is encrypted

Encryption Explored
- encryption and decryption are handled transparently
- encryption has a minimal impact on latency
- copying an unencrypted snapshot allows encryption (popular topic)
- snapshots encrypted
- yo ucan encrypt root device

4 Steps to encrypt and unencrypted volume
- create snapshot of unencrypted root device volume
- create a copy of the snapshot and select the encrypt option
- create an ami from the encrypted snapshot
- use that ami to launch a new encrypted instance

Demo
- ec2 launch instance
- create a snapshot
- copy snapshot and choose encryption
- actions -> create an image from ebs snapshot
- under AMIs -> Launch

Exam Tips
- data at rest is encrypted in the volume
- data in flight encrypted
- volumes and snapshots encrypted
- need to create a snapshot then copy then encrypt and then create AMI and use to launch