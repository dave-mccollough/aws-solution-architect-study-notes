# S3 Storage Classes

- **S3 Standard**
    - Highly available and Durable
        - Data is stored redundantly across multiple devices and facilities (>= 3 Availability Zones)
            - **99.99% Availability**
            - **99.999999999% Durablity (11 9's)**

    - Designed for frequently access data
    - Suitable for most workloads
        - Default S3 storage class
        - Use Case:
            - Websites
            - Content Distribution
            - Big Data Analytics


- **S3 Standard-Infrequent Access (S3 Standard-IA)**
    - Designed for **infrequently accessed** data
        - Used for data that requires rapid access, but is accessed less frequently
    - You pay to access the data
        - There is a low per GB storage price and a per GB retrieval fee
    - Use Case:
        - Long term storage
        - Backups
        - Data store for disaster recovery files


- **S3 One Zone-Infrequent Access (S3 One Zone-IA)**
    - Just like S3 Standard-IA, but data is stored redundantly within a single availability zone
    - Costs 20% less than regular S3 Standard-IA
    - 99.5% Availability
    - 99.999999999% Durability (11 9's)
    - Use Case:
        - Long lived, infrequently access, non-critical data

- **S3 Intellignet Tiering**
    - Automatically moves your data to the most cost effective tier based on how frequently you access each object
    - 99.99% Availability
    - 99.999999999% Durability (11 9's)
    - Use Case
        - Unknown or unpredictable access patterns

## Glacier
- Cheap storage
- Use only for infrequently accessed data
- Pay each time you access the data
- Use for data archival
- 99.99% Availability
- 99.999999999% Durability (11 9's)

- **S3 Glacier**
    - Provides long-term data archiving
    - Retrieval times range from 1 minute to 12 hours
    - Use Case:
        - Historical data only accessed a few times a year

- **S3 Glacier Deep Archive**
    - Provides lon-term data archiving
    - Default retrieval time of 12 hours
    - Use Case:
        - Historical data only accessed once or twice a year