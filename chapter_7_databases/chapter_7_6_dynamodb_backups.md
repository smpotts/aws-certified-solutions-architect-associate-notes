# Saving your Data with DynamoDB Backups

On Demand Backup and Restore
- full backups at any time
- 0 impact on table performance or availability
- retained until deleted
- same region as source table

Point in Time Recovery
- protects against accidental writes or deletes
- restore to any point in the last 35 days
- not enabled by default
- latest restorable time is 5 minutes in the past
- incremental backups


