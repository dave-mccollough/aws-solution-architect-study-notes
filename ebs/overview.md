# EBS Overview

## Elastic Block Store (EBS)

- Storage volumes that can be attached to an EC2 instance (virtual hard disk)

  - Install Operating System
  - Create File System
  - Install Applications
  - Store Files

- Designed for mission critical, production workloads
- Highly Available: Automatically replicated within a single availablity zone to protect against hardware failures
- Scalable. Dymanically change volume size or type with no downtime or performance impact to your systems
  - You may have to resize file system

## Volume Types

**General Purpose SSD (GP2)**

- Balance of price and performance
- 3 IOPS per GB, up to 16,000 IOPS per volume
- Volumes smaller than 1 TB can burst up to 3,000 IOPS
- Good for boot volumes or development/test applications that are not latency sensitive

**General Purpose SSD (GP3)**

- Predictable 3,000 IOPS baseline performance at 125 MB/s regardless of volume size
- Ideal for applications that require high performance and low cost
  - MySQL
  - Virtual Desktops
  - Hadoop Analytics
- Users can scale up to 16,000 IOPS and 1,000 MB/s for an additional fee

**Provisioned IOPS SSD (io1)**

- High performance, most expensive
- Up to 64,000 IOPS per volume
- 50 IOPS per GB
- **Use if you need more than 16,000 IOPS**
- **Designed for I/O intensive applications (Databases, latency sensitive workloads)**

**Provisioned IOPS SSD (io2)**

- Same price as io1
- Latest generation
- Higher durability and more IOPS
  - 500 IOPS per GB up to 64,000 IOPS
  - 99.999% durability (instead of 99.9%)
- **Designed for I/O intensive applications (Databases, latency sensitive workloads)**

**Throughput Optimized HDD (st1)**

- Low cost HDD volume
- Baseline 40 MB/s per TB throughput
- Burst up to 250 MB/s per TB
- Maximum throughput of 500 MB/s per volume
- Designed for frequently accessed, throughput intensive workloads
  - Big data, data warehouses, ETL, log processing
  - Good for storing large amounts of data
- **Cannot be a boot volume**

**Cold HDD (SC1)**

- Lowest cost option
- Baseline 12 MB/s per TB throughput
- Burst up to 80 MB/s per TB
- Maximum throughput of 250 MB/s per volume
- Designed for applications where performance is not a factor
  - File server
- **Cannot be a boot volume**

## IOPS vs Throughput

**IOPS**

- Measures number of read/write operations per second
- Important metric when tracking latency for high transaction workloads
- Execute reads/writes quickly
- If high throughput is a requirement, choose Provisioned IOPS SSD (io1 or io2)

**Throughpu**

- Measures number of bit read/written per second
- Important metric for large datasets and complex queries
- If dealing with large datasets is a requirement, choose Throughput Optimized HDD (st1)
