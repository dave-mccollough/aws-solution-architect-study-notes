# DynamoDB Backups

- On-demand backup and restore
    - Full backups at any time
    - Zero impact on table performance or availability
    - Consistent within seconds and retained until deleted
    - Operates within the same region as the source table

- Point-in-Time-Recovery (PITR)
    - Protects against accidental writes or deletes
    - Restore to any point in the last 35 days
    - Incremental backups
    - Not enabled by default
    - Latest restorable time is 5 minutes in the past