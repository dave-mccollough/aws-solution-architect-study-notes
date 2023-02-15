# Read Replicas

- A read replica is a read-only copy of your primary database
- When your application does a query, it would query the read replica and not your database, reducing load on your database
- Use for read-heavy workloads - takes the load off your primary database
- Read replicas can cross different availablity zones or regions
- Each read replica has it's own DNS endpoint
- Read replicas can be promoted to be their own databases 
    - This breaks replication between the replica and primary database
- Automatic backups must be enabled to deploy a read replica
- Multiple read replicas are supported
    - MySQL, MariaDB, PostgreSQL, Oracle and SQL Server
    - Add up to 5 read replicas to each database instance



- **Multi-AZ is for disaster recovery, read replicas are for scaling and improving performance**
    - Multi-AZ is an exact copy of your production database
    - Used for disaster recovery
    - RDS will automatically fail over to standby instance in the event of a failure

