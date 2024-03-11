# Volumes and Snapshots

What are Volumes?
- volumes exist of EBS
- virtual hard disks
- need a minimum of 1

What are Snapshot?
- snapshots exist on s3
- a photo of the volume
- point in time copy of a volume
- snapshots are incremental
	- saves on spaces and time
- first snapshot is slow

3 Tips for Snapshots
- consistent snapshots: stop the instance and take a snap
	- gets things that are locally cached
- encrypted snapshots
- sharing snapshots: only in the region they were created
	- have to create a copy and then move it to another region

What to Know about EBS Volumes
- EBS volumes will always be in the same AZ as EC2
- resizing and change types on the fly

Demo
- root device volume is added already, gp2 by default
- create a snapshot
- actions -> copy -> destination region 
	- you can encrypt it as well
- switch regions and see the snapshot in the other region
- actions -> create an ec2 image to another region
	- how you can migrate an ec2 instance from one region to another
*popular topic

Exam Tips : 5 things to remeber
1. volumes exists on ebs, snapshots are on s3
2. snapshots are photos of volumes, incremental
3. first one is slow
4. you can share snapshots by making a copy
5. you can resize or change types on the fly
