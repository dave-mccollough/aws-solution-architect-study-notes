# S3 Encryption

## Types or Encryption

- **Encryption in Transit**
    - SSL/TLS
    - HTTPS

- **Encryption at Rest: Server-Site Encryptio**
    - **SSE-S3:**  S3 managed keys, using AES 256-bit encryption (most common)
    - **SSE-KMS:**  AWS Key Management Service managed keys
    - **SSE-C:** Customer Provided Keys

- **Encryption at Rest: Client-Side Encryption**
    - Encrypt files before uploading them into S3

## Enforcing Server-Side Encryption
- **Console**
    - Select the encryption setting on your S3 Bucket
    - Easiest method - checkbox in console
- **Bucket Policies**
    - Enforce encryption using a bucket policy
    - Deny all **PUT** requests that don't include the `x-amz-server-side-encryption` parameter in the request header