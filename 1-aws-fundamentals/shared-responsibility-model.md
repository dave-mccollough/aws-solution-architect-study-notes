# Shared Responsibility Model

## Amazon's Responsibility

### Infrastructure
- Regions
- Availabilty Zones
- Edge Locations

### Software
- Compute
- Storage
- Databases
- Networking

## Customer Responsibiltiy

### Operating System, Network and Firewall Configuration
- Client side data encryption and data intergrity authentication
- Server-side encryption
    - File system and/or data
- Networking traffic protection

### Platform, Applications, Identity and Access Management

### Customer Data

### Exam Tips:
- Ask your self if you can do this in the AWS console.
    - If yes, you are likely responsible
        - Security groups
        - IAM users
        - OS patching
        - Database patching

    - if no, AWS is likely responsible
        - Data center management
        - Data center security
        - Data center cabling

Encryption is a **Shared Responsibility**

