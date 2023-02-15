# Lifecycle Management

## What is Lifecycle Management
- Lifecycle management automate moving your objects between different storage tiers, maximizing cost effectiveness
- Example
    - Keep object in S3 Standard for 30 Days
    - Move object to S3 IA after 30 Days
    - Move object to Glacier after 90 Days

- Lifecycle management can be used with versioning to move different versions of objects to different storage tiers
- Can be applied to current and previous versions of objects

## To Enable Lifecycle Management
- Browse to the bucket you want to enable Lifecycle Management on
- Click **Management** tab
- Click **Create lifecycle rule** button
![](2021-12-12-14-43-14.png)