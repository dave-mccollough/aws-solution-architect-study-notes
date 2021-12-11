# Managing IAM Credentials

## Building Blocks of IAM
- IAM is universal - does not apply to a specific region

### Users
- A physical person
- Users have no permissions when first created

### Groups 
- Contains users
- Users should inherit permissions from groups
- Based on job functions
    - Developer
    - Administrator
- IAM policy documents should be applied to groups, not users

### Roles
- Internal to AWS
- Allows one AWS resource to access another AWS resouce

## Principle of Least Privilege
- Only assign a user the minimm amount of privileges they need to do their job

## Access Types
- Access Key/Secret Access Key
    - Provides programmatic access to the AWS API, CLI, SDK and other development tools
    - Not the same as username and password
    - Only get to view these when the user is created.  
    - If you lose them, you will need to regenerate them, so save them in a secure location.

- Password
    - Enables a user to use a password to login to the AWS console

## Passwords
- You can create and customize password rotation policies

## IAM Federation
- Using an existing user account and credentials (usually Active Directory) to login to AWS.

## Identity Federation
- Uses SAML standard (Active Directory)
