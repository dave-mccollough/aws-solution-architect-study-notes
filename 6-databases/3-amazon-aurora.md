# Amazon Aurora

- Amazon Aurora is a MySQL and PostgreSQL compatible relational database engine
- Combines speed and availability of commerical database with the cost-effectiveness of open-source databases
- 5x better performance with MySQL and 3x better performance than PostgreSQL at a much lower pricepoint
- Propietary Amazon database

- Starts in 10GB size, scales to 128TB in 10GB increments (Storage Auto Scaling)
- Compute resources can scale up to 96vCPUs and 768GB of memory
- Two copies of your data are contained in each availabity zone, with a minimum of 3 availability zones (6 copies of your data)
- Aurora is designed to handle the loss of up to 2 copies of data without affecting database write availability and up to 3 copies without affecting read availability
- Aurora storage is self-healing.  Data blocks and disks are continously scanned for errors and repaired automatically

- Three different types of Aurora replicas available
    - Aurora Replicas
        - 15 Read replicas
        - In region replica location
        - Automated failover
        - No data loss at failover
        - No support for different data or schema vs primary
    - MySQL Replicas
        - 5 read replicas
        - Cross-region replica location
        - No automated failover
        - Support for different data or schema vs primary
    - PostgreSQL replicas
        - 5 read replicas

- Backups
    - Automated backups are always enabled with Aurora DB instances
    - Backups do not impact performance
    - You can take snapshots 
        - Snapshots do not impact performance
        - Aurora snapshots can be shared with other AWS accounts

- Aurora Serverless
    - On-demand, auto-scalling configuration for the MySQL and PostgreSQL compatible versions of Aurora
    - Aurora serverless DB clusters startup, shutdown, scale up/down based on application needs
    - Only pay for what you use

    - Use Cases
        - Infrequent, intermittent, or unpredictable workloads
