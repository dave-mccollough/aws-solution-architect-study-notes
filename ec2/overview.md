# EC2 Overview

## Elastic Compute Cloud (EC2)

- Secure, resizable compute capacity in the cloud
- Like a VM, only hosted in AWS
- Designed to make web-scale cloud computing easier
- the capacity you want, when you need it
- **You are in control of your own instances (patching, etc)**
- You only pay for what you use
  - Scale capacity as needed

## EC2 Pricing Options

- **On-Demand**

  - Pay by the hour or second based on the instance you are running
  - Flexible - No long term commitment
  - Use Case:
    - Applications with short term, spiky, or unpredictable workloads that can't be interrupted
    - Applications being developed or tested on Amazon EC2 for the first time

- **Reserved**

  - Reserve capacity for 1-3 years. Up to a 72% discount on the hourly charge
  - You can pay upfront to futher reduce total computing costs
  - Reserved instances operate at a regional level, so you can transfer a RI to a different region
  - Can be used with Lambda and Fargate
  - Types of reserved instances
    - Standard
      - Up to 72% off on-demand price
    - Convertible
      - Up to 54% off on-demand price
      - Has the option to change to a different reserved instance type of equal or greater value
    - Scheduled
      - Instance launches within the time window you define
      - Match your capacity reservation to a predictable recurring schedue
  - Use Case:
    - Applications with predictable usage
    - Applications that require a reserved capacity

- **Spot**

  - Purchase unused capacity at a discount of up to 90%. Prices fluctuate with supply and demand
  - Use Case:
    - Applications that have flexible start and end times
    - Applications that are only feasible at very low compute prices
    - Urgent need for large amounts of computing capacity
      - Image Rendering
      - Genomic Sequencing
      - Alogrithmic Trading engines

- **Dedicated Hosts**
  - A physical EC2 server dedicated to your use. The most expensive option
  - Can be purchased on-demand or hourly
  - Use Case:
    - Compliance
      - Regulatory requirements that may not support multi-tenant virtualization
    - Licensing
      - Applications or licensing that does not support multi-tenancy or cloud deployments
