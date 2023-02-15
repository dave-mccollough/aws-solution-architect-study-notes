# Spot Instances

- Spot instances allow you to take advantage of unused EC2 capacity. Spot instances can be discounted up to 90% compared to on-demand pricing
- Spot instances should be used for stateless, fault tolerant, or flexible applicaitons or anywhere you don't need persistent storage

  - Big Data
  - Containarized workloads
  - HPC
  - Test/Dev workloads

- Spot blocks can be used to block Spot instances from being terminated
- Spot fleet is a collection of Spot instances and (optionally) On-Demand instances
