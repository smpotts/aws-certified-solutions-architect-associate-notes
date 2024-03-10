# Chapter 4.5 S3 Storage Classes

Will be given scenarios where you will have to pick tier

S3 Standard
- highly available and durable
- at least 3 AZs
- 99.99 availability
- 11 9's durability
- designed for frequent access
- suitable for most workloads
- static websites
- content distribution

S3 Standard - Infrequent Access
- used for data accessed less frequently but need it fast when we need it
- need long term storage, minimize cost but need it fast

S3 One Zone - Infrequent Access
- like s3 standard IA but data stored redundantly within one AZ
- only use when you can afford to lose the data but want to minimize cost
- 20% less than standard

S3 Intelligent Tiering
- moves data to the most cost effective tier depending on how much you access the data

Glacier
- archive data long term
- pay for each time you access data
- cheap

Glacier Instant Retrieval
- long term data archiving with instant retrieval time

Glacier Flexible Retrieval
- doesn't need immediate retrieval, could be up to 12 hours

Glacier Deep Archive
- customers that have to retain data sets for 7+ years
- standard retrieval time is 12 hours but bulk retrieval is 48 hours
- cheapest storage class

Pricing
- standard most expensive
- intelligent tiering cost optimizes
- retrieval fee applies to IA tiers
- retrieval fee applies to glacier tiers too
- deep archive is cheapest
- deep archive retrieval could be up to 48 hours

Exam Tips
- need to know storage types and use cases
