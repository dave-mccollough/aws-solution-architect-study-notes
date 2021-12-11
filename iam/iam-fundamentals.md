# Idenity and Access Management (IAM)

## What is IAM
- IAM stands for Identity and Access Management
- Allows you to manage users and their level of access to the AWS Console
    - Create users and assign permissions to those users
    - Create groups and roles
    - Control access to AWS resources

- IAM starts with the Root Account

## What is the Root Account?
- The **root account** is the email address used to sign up for the AWS.  
- The root account has **full administrative access** to AWS.
- It's important to secure this account
- **Do not** use the root account to login to the AWS console on a daily basis.

## Securing a root account
1. Enable MFA on the root account.
2. Create an admin group for administrators.
3. Assign appropiate permissions to the admin group created in step 2.
4. Create user accounts for administrators.
5. Add users accounts to the admin group

## Notes
- Configure MFA on the root account
    - Login to the AWS Console 
    - Browse to the IAM Dashboard
    - Select the root user
    - Select the **Security credentials** tab
    - Follow instructions to configure MFA

