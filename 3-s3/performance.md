# Optimizing S3 Performance

## S3 Prefixes 
- Folders inside a bucket
- https://daves-bucket.S3.Region.amazonaws.com/**folder-one**/mountain.jpg
- https://daves-bucket.S3.Region.amazonaws.com/**folder-one**/**subfolder-two**/mountain.jpg


## S3 Performance
- 3,500 requests per second for **PUT/COPY/POST/DELETE**
- 5,500 requests per second for **GET/HEAD**
    - The more folder and subfolders you have in your S3 bucket, the better the performance
    - You can get better performance by spreading your reads across different prefixes
    - If you are using two prefixes, you can achieve 11,000 requests per second

## KMS Limits
If using SSE-KMS to encrypt your objects in S3, keep in mind KMS limits
- Uploading/Downloading will count toward quota
- Limited to 5,000, 10,000, 30,000 requests per second depending on region
- Currently you can't request a quota increase for KMS


## S3 Uploads
### Multipart Uploads
- Recommended for files **over 100MB**
- Required for files **over 5GB**
- Parallelize uploads (increase efficiency)

## S3 Downloads
### S3 Byte-Range Fetches
- Speed up downloads
    - Parallelize downloads by specifying byte ranges
    - If there's a failure in the download, it's only for a specific byte range
- Can be used to download partial amounts of a file
