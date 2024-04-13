Chapter 13.4 Ordered Messages with SQS FIFO

SQS Message Ordering
- in a Standard SQS queue they might return the messages out of order
	- might even get a message twice
- when ordering and duplication matters, you want a FIFO queue
	- guarantees ordering and that there are not duplicate messages

Standard SQS
- best effort ordering
- nearly unlimited transacations per seconds
- duplicates messages

FIFO SQS
- more expensive
- only 300 messages per second
- guaranteed ordering
- no duplication

Console Demo
- FIFO queue names have to end in .fifo
- message group id tags messages so they are all in the same group
- message deduplication id ensures that the messages are all unique
- the same message sent multiple times will only show up in the queue once

Exam Tips
- fifo is the only option for message ordering
- fifo is the only way this will come up on the exam
- fifo doesn't have the same level of performance
- not the only way to order messages but it's more work and reqs a custom setup
- message group id ensures messages are processed one by one
- fifo does cost a little more money
