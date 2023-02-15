# Networking with EC2

## Three (3) diffferent types of virtual networking options are available for EC2 instances

**ENI: Elastic Network Interface**

- For basic, day to day networking
- Attached by default to an EC2 instance
- Private IPv4 Addresses
- Public IPV4 Addresses
- Many IPv6 Addresses
- MAC Addresses
- 1 or more Security Groups
  - Virtual firewall in the cloud
- **ENI Use Cases:**
  - Create a management network
  - Use network or security appliances in your VPC
  - Create dual-homed instances with workloads/roles on distinct subnets
    - Allows for private network addresses
  - Create a low budget, highly available solution

**EN: Enhanced Networking**

- For high performance networking between 10Gbps and 100Gbps
- Uses single root I/O virtualization(SR-IOV) to provide higher I/O performance with lower CPU utilization
- Provides higher bandwidth and higher packet per second (PPS) performance
- Lower inter-instance latencies
- **Two options to enable enhanced networking** - **Enhanced Network Adapter(ENA)** - Supports network speeds up to 100Gbps for supported instance types - **Intel 8259 Virtual Function(VF) interface** - Supports network speeds up to 10Gbps for supported instance types - Typically used in older instances
  **EFA: Elastic Fabric Adapter**
- Accelerates high performance compute(HPC) and machine learning applications
- Provides lower and more consistent latency throughput than the TCP transport typically used in cloud based HPC systems
- **OS-BBYPASS**
  - OS-Bypass enables HPC and machine learning compute applications to bypass the operating system kernal and communicate directly with the EFA device
  - Only supported in Linux
