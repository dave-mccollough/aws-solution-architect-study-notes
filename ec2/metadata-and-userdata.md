# EC2 Metadata and User data

- EC2 metadata is data about your EC2 instance

  - It can include private and public IP addresses, hostnames, security groups, etc.

- You can use the `curl` command to query EC2 metadata

  - `curl http://169.254.169.25/latest/meta-data/`

- User data is bootstrap scripts

- You can use bootstrap scripts to access metadata
