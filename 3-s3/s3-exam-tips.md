# S3 Exam Tips

- S3 is object based. You can only upload files, not install software.
- File size can be from 0 to 5 TB
- Total volume of data and number of objects you can store is unlimited.

- S3 is a universal namespace
- Bucket URL:
  - https://bucket-name.s3.region-name.amazonaws.com/key-name
  - https://daves-bucket.s3.us-east-1.amazonaws.com/mountain.jpg

**Key:** The object name (mountain.jpg)
**Value:** The data
**Version ID:** Allows you to store multiple versions of the same object.
**Metadata:** Data about the data you are storing (`last-modified`, `content-type`)

## Securing your bucket

- Buckets are private by default. You have to allow access to both the bucket and objects in the bucket for access
- You can make individual objects public by using **Access Control Lists (ACL)**.
- You can make entire buckets public using bucket policies.
- When you succesfully upload an object, S3 will return a HTTP 200 code

## Hosting a static website

- You can make entire buckets public using bucket policies.
- You can use S3 to host static content
- S3 automatically scales with demand

## Versioning

- All versions of an object are stored in S3, including all writes and deletes.
- Once enabled, versioning can't be disabled.. only suspended.
- Versioning can be integrated with lifecycle rules.
- Support for MFA

## Storage classes

- 6 different storage tiers and use cases:
  - **S3 Standard:** Suitable for most workloads
  - **S3 Infrequently access:** Long term, infrequently accessed **critical** data.
  - **S3 One Zone-Infrequent Access:** Long term, infrequently accessed **non-critical** data.
  - **S3 Glacier:** Long-term data archiving that occassionally needs to be accessed withing a few hours or minutes.
  - **S3 Glacier Deep Archive:** Rarely accessed data archiving, with a default retrieval time of 12 hours.
  - **S3 Intelligent- Tiering:** Unknown or unpredictable access patterns

## S3 Object lock

- Use S3 Object lock to store objects using a write once, read many (WORM) model.
- Object lock can be on individual objects or applied across the bucket as a whole.
- Obhject lock comes in two modes: Governance and Compliance mode
  - **Governance Mode:** Users can't overwrite or delete an object version or alter it's lock settings without special permissions.
  - **Compliance Mode:** A protected object version that can't be overwritted or deleted by any user, including the root user of your AWS account.

## Glacier Vault Lock

- Allows you to deploy and enforce compliance controls for individual S3 glacier vaults with a vault lock policy.
- You can specify controls, such as WORM, in a vault lock policy
- Once locked, the policy can no longer be changed.

## Encryption

- Encryption in transit

  - SSL/TLS
  - HTTPS

- Encryption at Rest: SSE

  - Server-side encryption
  - SSE-S3 (AES 256-bit)
  - SSE-KMS
  - SSE-C

- Client-Side encryption

  - You encrypt the files before uploading to S3.

- Enforcing encryption with a bucket policy
  - A bucket policy can deny all PUT requests that don't include the `x-amz-server-side-encryption` parameter in the request header.

## Optimzing performance

- S3 Prefixes

  - Folders inside a bucket
    - https://daves-bucket.S3.Region.amazonaws.com/**folder-one**/mountain.jpg
    - https://daves-bucket.S3.Region.amazonaws.com/**folder-one**/**subfolder-two**/mountain.jpg

- 3,500 requests per second for **PUT/COPY/POST/DELETE**
- 5,500 requests per second for **GET/HEAD**

  - The more folder and subfolders you have in your S3 bucket, the better the performance

- You can get better performance by spreading your reads across different prefixes

  - If you are using two prefixes, you can achieve 11,000 requests per second

- If using SSE-KMS to encrypt your objects in S3, keep in mind KMS limits
  - Uploading/Downloading will count toward quota
  - Limited to 5,000, 10,000, 30,000 requests per second depending on region
  - Currently you can't request a quota increase for KMS

## S3 Uploads

- User multipart uploads to increase performance when uploading files to S3
  - Recommended for files **over 100MB**
  - Required for files **over 5GB**
  - Parallelize uploads (increase efficiency)

## S3 Downloads

- Use S3 Byte-Range Fetches to speed up downloads
  - Parallelize downloads by specifying byte ranges
  - If there's a failure in the download, it's only for a specific byte range

## S3 Backup

- Use S3 replication to backup data
  - You can replicate objects from one bucket to another
  - Objects in an existing bucket are not repilcated automatically
  - Delete markers are not replciated by default
