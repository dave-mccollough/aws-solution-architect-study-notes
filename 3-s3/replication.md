# S3 Replication

- **S3 Replication allows you to replicate objects from one bucket to another**
    - Versioning must be enabled on both source and destination buckets
    - Objects that existed in a bucket before replication was turned on will not be replicated automtically.  
    - Subsequent items added after replication was turned on will be replicated automatically
        - **create two new buckets (source and destination buckets), then upload your files
    - Delete markers are not replicated by default

## To enable Replication**
- Browse to the bucket you want to enable replication on
- Click **Management** tab
- Scroll to **Replication rules** section
- Click **Create replication rule** button
![](2021-12-12-15-47-33.png)

