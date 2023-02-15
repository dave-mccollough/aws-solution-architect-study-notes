# Amazon Machine Images (AMI) - EBS vs. Instance Store

**What is an AMI**

- AMI's provide the information necessary to launch an instance
- AMI's are considered a blueprint for an EC2 instance
  - AMI's must be specified to launch an instance

**5 Things you can base your AMI on:**

- Region
- Operating System
- Architecture (64 or 32 bit)
- Launch Permissions
- Root device storage

**AMI Catagorization**

- AMI's are catagorized as backed by EBS or Instance Store

  - **Instance Store**

    - Sometimes called ephemeral storage
    - Cannot be stopped. If the host is stopped, data will be lost
    - Can be rebooted without data loss
    - Root volume is delated on termination

  - **EBS**
    - Can be stopped. If stopped, data will not be lost
    - Can be rebooted without data loss
    - Root volume is deleted on termination, but you can tell AWS to save root volume
