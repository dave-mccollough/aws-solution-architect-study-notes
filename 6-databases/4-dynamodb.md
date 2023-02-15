# DynamoDB 

- NoSQL database service for applications that need millisecond latency at any scale
- Fully managed
- Supports document and key-value data models
- Pay per request pricing
- Balance of cost and performance
- No minimum capacity
- Pay more per request than with provisioned capacity
- Use cases include: Mobile, gaming, web, IoT, ad-tech, new product launches, etc.

- Stored on SSD storage
- Spread across three geographically distinct data centers
- Eventual consistent reads by default
    - Consistency across all copies of data is usually reached within a second
    - Repeating a read after a short time should return updated data
    - Best read performance

- Strongly consistent reads available
    - Returns a result that reflects all writes that received a successful response prior to the read

- DynamoDB Accelerator (DAX)
    - Fully managed, highly available, in-memory caching service for DynamoDB
    - 10x performance improvement
    - Reduces request times from milliseconds to microseconds even under load
    - Developers don't need to manage caching logic
    - Compatible with DynamoDB API calls

- Security
    - Encryption at rest using KMS
    - Site to Site VPN
    - IAM Policies and roles
    - Fine grained access
    - Integrates with CloudWatch and CloudTrail
    - VPC Endpoints
