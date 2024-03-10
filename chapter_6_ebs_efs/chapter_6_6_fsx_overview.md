# FSx Overview

FSx for Windows
- fully managed native Microsoft windows file system
- can move windows to AWS

FSx for Windows vs EFS
- FSx for windows  is designed for Windows and Windows apps
- EFS is for ec2 instances based in NFS
- migrating sharepoint or active directory -> FSx

FSx for Lustre
- fully managed file system optimized for compute intensive jobs

FSx for Lustre Performance
- processing massive data sets, low latency, IOPS, AI, ML

Exam Tips
- EFS: when you need distributed, highly resistenly storage for Linux instances and Linux based applications
- FSx for Windows: centralized storage for Windows based applications i.e. SharePoint, SQL Server, Workspaces, etc
- FSx for Lustre: high speed, high capacity, distributed storage, can store data directly on S3