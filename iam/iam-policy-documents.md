# IAM Policy Documents

## Permissions with IAM
- Permissions are assigned using policy documents.
- Policy Documents are made up of JSON (JavaScript Object Notation).
    - Key/Value Pairs

- Policy document example for full admin access: 
    {
        "Version" : "2012-10-17",
        "Statement" : [
            {
                "Effect" : "Allow",
                "Action" : "*",
                "Resource" : "*"
            }
        ]
    }
     - Effect: Allow or Deny
     - Action:  What the user can do
     - Reource:  What resource is impacted

- IAM Policy Documents can be assigned to:
    - Groups
    - Users
    - Roles
