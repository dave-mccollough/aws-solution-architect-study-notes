# DynamoDB Transactions

- ACID for Databases
- All or nothing transactions
- Transaction either succeeds across all tables or the entire transaction fails

    - Atomic
        - All changes to the data must be performed successfully or not at all
    - Consistent
        - Data must be in a consistent state before and after the transaction
    - Isolated
        - No other process can change the data while the transaction is running
    - Durable
        - The changes made by a transaction must perisist

- DynamoDB Transactions provide developers ACID across one or more tables within a single AWS account and region
- Up to 25 items or 4MB of data per transaction

- Three options for reads
    - Eventual
    - Consistency
    - Transactional

- Two options for writes
    - Standard
    - Transactional

- Use cases 
    - Processing financial transactions
    - Fulfilling and managing orders
    - Building multiplayer games
    - Coordinating actions across distributed components or services

