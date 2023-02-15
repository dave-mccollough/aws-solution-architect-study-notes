# EFS Overview

## Elastic File System (EFS)

- Can be mounted on many different EC2 types
- Works with EC2 instances that are in multiple availablity zones
  - Centralized/shared storage for multiple EC2 instances
- Highly available and scalable
- Expensive
- Uses NFSv4 protocol
- Compatible with Linux based AMI (Windows support currently not available)
- Encryption at rest using Key Management System (KMS)
- Auto-scaling file system - no capacity planning
- Pay per per - Expensive

**Performance**

- 1000's of concurrent connections from EC2 instances
- 10GB/s throughput
- Abiltiy to scale storage to petabytes
- EFS performance characteristics can be set during setup
  - General Purpose
    - Web servers, CMS, etc
  - Max I/O
    - Big data, media processing, etc.

**Storage Tiers**
EFS provides storage tiers and lifecycle management allowing you move data from one tier to another based on parameters you setup

- Standard Storage Tier: For frequently accessed files
- Infrequent Accessed: For files not frequently accessed

**Use Cases**

- Content Management
- Web Servers
