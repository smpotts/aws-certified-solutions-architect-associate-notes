# Chapter 7.5 When Do We Use DynamoDB Transactions?

ACID Diagram
- atomic, consistent, isolated, durable
- A all changes must be performed successfully or not at all
- C data must be in a consistent state before and after transaction
- I nothing can change the data while the transaction is running
- D changes made by a transaction must be persistent

ACID with DynamoDB
- can use ACID with DynamoDB but must use DynamoDB transactions
- when things require coordinated inserts, deletes, updates to multiple items
- ACID provides devs atomicy, consistency, durability and isolation across 1 or more tables within an AWS account and region

**scenario based question asking about using ACID with DynamoDB -> TRANSACTIONS

All or Nothing
*ACID means all or nothing!

Use Cases
- processing financial transactions
- managing and fulfilling orders
- building multiplayer game engines
- coordinating actions across distributed components and services

Transactions
- multiple all or nothing operations
- 3 options for reads: eventual, strong or transactionsal
- 2 options for writes: standard and transactional
- up to 25 items per go

Exam Tips
- DynamoDB transactions : ACID reqs
- atomicity, isolation, durability and consistency
- transactions are all or nothing
