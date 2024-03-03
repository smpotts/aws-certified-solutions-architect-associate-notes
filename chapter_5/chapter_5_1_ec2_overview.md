EC2 Overview

**comes up on the exam a lot!

Elastic Compute Cloud (EC2)
- secure, resizable compute in the cloud
- it's a virtual server
- designed to make web-scale computing easier
- gives you capacity you want when you need it
- you are in complete control
- only pay for what you use
- no wasted capacity

EC2 Pricing Options
1. on-demand: pay by t he hour or second depending on the instance type you run
2. reserved: reserved for 1-3 years, most discounted
3. spot: unused capacity at a 90% discounted price but the price fluxuates
4. dedicated: you have a physical ec2 server for your use, most expensive

On-Demand Instances
- need low cost and flexibility
- no upfront payment or longterm commitment
- short term
- building a POC
- testing the waters

Reserved Instances
- 1-3 years
- super flexible
- predictable usage
- specific capacity requirements
- you're able to pay upfront
- standard reserved instances: up to 72% off the on-demand price if you pay it all upfront
- convertible reserved instances: you have the option to changes to different reserved instances of equal or greater value, 54% savings
- scheduled reserved instances: launch within time window you define, predictable recurring schedule that only requires a fraction of time window
- operate at regional level

Spot Instances
- you say which price you want to have spot instances at and when it hits that price you get the instance
- really good for cost sensitive applications
- urgent need for large amounts of additional computing capacity
- trying to save the most amount of money
- not for things requiring a lot of up time

Dedicated Instances
- compliance requirements that don't support multitenant virtualization
- licensing that doesn't support multitenant or cloud deployments
- can be purchased on demand
- can reserve them for up to 70% off the on-demand price

Exam Tips
- EC2 is like a VM hosted in AWS instead of the data center
- only pay for what you use
- select capacity you need right now
- on demand: by the hour/ sec
- reserved: 1-3 years, 72% discount, known fixed reqs
- spot: unused capacity, price moves w/ supply and demand, flexible start and end times
- dedicated: compliance and licensing reqs
