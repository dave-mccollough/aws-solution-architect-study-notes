# S3 Object Lock

## What is S3 Object Lock
- You can use S3 Object lock to store objects using a write once, read many (WORM) model
- It can help prevent objects from being deleted or modified for a fixed amount of time, or indefinitely
- S3 Object lock can be used to meet regulatory requirements that require WORM storage, or add an extra layer of protection against object changes or deleteion

## S3 Object Lock Modes
- **Governance Mode**
    - Users can't overwrite or delete an object version or alter it's lock settings unless they have special permissions
    - Governance mode protects objects from being changed or deleted unless the user has permissions to do so
    - **Allows some users the ability to overwrite or delete an object version**

- **Compliance Mode**
    - Protected objects can't be overwritten or deleted by any user, including the root user of the AWS account
    - The objects retention mode can't be changed and it's retention period can't be shortened
    - Ensures the object version can't be overwritten or deleted for the duration of the retention period
    - **Blocks all users from overwriting or deleting an object version during the retention period**

## Retention Periods
- Protects an object version for a fixed amount of time
- After the retention period has expired, the object version can be overwritten or deleted unless you also place a legal hold on the object version.

## Legal Hold
- S3 Object lock that prevents an object from being overwritten or deleted.
- Remains in effect until removed
    - Legal holds do not have an associated retention period and can be freely assigned and removed by any user with the following permission:  `s3:PutObjectLegalHold`

# Glacier Vault Lock
- Allows you to deploy and enforce compliance controls for individual S3 Glacier Vaults with a vault lock policy
- Allows you to specify controls such as WORM in a lock policy and lock the policy from future edits
- Once locked, the policy can't be changed