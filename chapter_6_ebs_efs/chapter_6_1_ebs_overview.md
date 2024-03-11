# EBS Overview

What is EBS?
- elastic block storage
- different types of volumes, use cases for each type
- storage volume to attach ec2 instance to
- need a place where app, os and database are installed
- use them the same way you would a system disk
- virtual hard disk in the cloud

Mission Critical
- production workloads
- highly available
- automatically replicated in a single AZ
- scalable, dynamically increase capacity and change vollume type, no downtime

EBS Volume Types: SSD Solid state disk
1. General Purpose SSD (gp2) : good for boot volumes or development or test apps that are not latency sensitive, 
- balance of price and performance
- default volume
- can scales up
* there is a new gen (gp3)
2. Provisioned IOPS SSD (io1) : high performance option and the most expensive
* there is a new gen (io2) : higher durability and more IOPS, io intensive apps

EBS Volume Types: Hard Disk Drive
1. Throughput Optimized HHD
- low cost HHD
- frequently accessed and throughput intensive workloads
- big data, data warehouse, ETL, and log processing
- cannot be a boot volume
2. Cold HDD (sc1): lowest cost option
- good choice for colder data requiring fewer scans
- good for files server
- low cost when performance is not a factor
- cannot be a boot volume

** when you hear big data, ETL , think of throughput not IOPS

IOPS vs Throughput
IOPS
- measures the # of read and writes per second
- for quick transactional things, low latency apps
- action reads and write quickly
- if you have a transactional DB choose provisioned IOPS

Throughput
- measures the # of bits read or written per second
- deal with large data set
- complex queries, large data sets, large i/o
- if talking about db, etl, etc

Exam Tips
- ssd volumes: highly available and scalable storage volumes you can attach to your ec2 instance
- gp2: general purpose ssd: boot disks and general apps
- gp3: new version
- provisioned iops ssd io1: fast performance, online transaction processing, latency sensitive apps
- io2: new version

- st1: throughput ssd: etl, big data, cant be a boot volume
- sc1: cold hdd: less frequently accessed data, lowest cost
