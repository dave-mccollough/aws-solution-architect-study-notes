# EC2 Placement Groups

## Three types of placement groups

Logically group EC2 instances

**Cluster Placement Group**

- Grouping of instances within a single availablity zone
- Recommended for applications that need low network latency, high network throughput, or both (HPC)
- Only certain instance types can be launched into a cluster group
- Cluster placement groups **can't** span mulitple availablity zones

**Spread Placement Group**

- Group of instances placed on distinct underlying hardware
- Recommended for applications that have a small number of critical instances that should be kept seperate from each other
- Use for individual instances
- Spread placement groups **can** span multiple availablity zones

**Partition Placement Group**

- Each partion placement group has it's own set of server rack
- Each rack has it's own network and power source
- No two partions share the same rack, allow you to isolate the impact of a hardware failure within a application
- EC2 logically divides each group into logical segments called **partitions**
- Used for multiple instance with dedicated network and power sources

**Other notes**

- Only certain instance types can be launched into a placement group

  - Compute optimized
  - GPU
  - Memory optimized
  - Storage optimized

- Placement groups can't be merged
- AWS recommneds homogenous instances within a cluster placement group
- Existing instances can be moved into a placement group if they are in a stopped state
- Instance in placement groups can be removed via the AWS CLI or SDK (not console)
