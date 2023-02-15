# S3 Overview

## What is S3?
Simple Storage Service (3 S's = S3)

- **Object Storage**
    - Secure, durable, highly scalable object storage
    - Manages data as objects rather than in file systems or data blocks
    - Upload any file type
        - Photos, Videos, Docments, Text Files, Code
    - Cannot be used to run an operating sytem

- **Scalable**
    - Store and retrieve any amount of data from anywhere on the web at a very low cost

- **Simple**
    - Easy to use with a simple web interface

## S3 Basics
- Unlimited Storage
- Objects can be up to 5TB in Size
- Files are stored in 'buckets' (similar to folders)
- **Safe**
    - Data is spread across multiple devices and facilites to ensure **availabilty** and **durability**.

 **Univeral Namespace**
- Buckets have a Univeral Namespace
    - All AWS accounts share the S3 namespace, so each bucket name needs to be globally unique

**Bucket URLS**
- https://**bucket-name**.S3.Region.amazonaws.com/**key-name**
- Example:
    - https://daves-bucket123.S3.Region.amazonaws.com/mountain.jpg

**Uploading Files**
- When uploading a file to an S3 bucket, you will receive an **HTTP 200** code if the file upload was successful

**Key-Value Store**
- **Key**
    - The name of the object
- **Value**
    - The data (made up of a sequence of bytes)

- **Version ID**
    - Use for storing multiple versions of the same object

- **Metadata**
    - Data about the data you are storing
        - content-type
        - last-modified

**Highly Available and Durable**
- **High Availability**  
    - 99.95%-99.99% service availablity depending on S2 Tier

- **High Durability**
    - Designed for 99.999999999 (11 9's durability - 9 decimal places) durability for data stored in S3

**Tiered Storage**
- S3 offers a range of storage classes designed for different use cases

**Lifecycle Management**
- Define rules to automatically transition objects to a cheaper storage tier or delete objects that are no longer required after a set period of time

**Versioning**
- With versioning enabled, all versions of an object are stored and can be retrieved, including deleted objects


## Securing Data in S3
- **Server-Side Encryption
    - You can default encryption on a bucket to encrypt all new objects when they are stored in a bucket

- **Access Control Lists (ACLs)**
    - Define which AWS accounts or groups are granted access and the type of access.
    - ACLs can be attached to individual objects within a bucket

- **Bucket Policies**
    - Specify what actions are allowed or denied 
    - Allow user to **PUT** but not **DELETE** objects in a bucket

## Data Consistency
- Strong Read-After-Write Consistency
    - **After a successful write** of a new object (PUT) or an overwrite of an existing object, any subsequent read request immediately receives the latest version of the object
    - **Strong Consistency** for list operations
        - After a write operation, you can immediately perform a listing of the objects in a bucket with all changes reflected

