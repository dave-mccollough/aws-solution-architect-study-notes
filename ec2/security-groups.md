# Security Groups

- Security groups are virtual firewalls for a EC2 instance. By default, everything is blocked.
- To communicate with an EC2 instance via HTTP, SSH, or RDP, you will need to open the correct ports
  **To let all traffic access your EC2 instance, use 0.0.0.0/0.** **This is not recommended in a production enviornment**
- Changes to security groups take effect immediately
- You can have any number of EC2 instances in a security group
- Multiple security groups can be attached to one EC2 instance
- All inbound traffic is blocked by default
- All outbound traffic is allowed

## Bootstrap Scripts

- Bootstrap scripts run when an instance first starts
