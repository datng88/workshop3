---
title : "Create a bucket"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : " <b> 2.1 </b> "
---
1. In the **AWS Management Console**. Enter and select **S3** in search bar
![iam-1](/images/2-Prerequiste/2.1-createbucket/s3-1.png)
2. Choose **Create bucket**
![iam-1](/images/2-Prerequiste/2.1-createbucket/s3-2.png)
3. In the **Create bucket** details
   - **Bucket name:**  `myBucket                   `
   - **Bucket key**: Disable
   - Choose **Create bucket**
{{% notice note %}}
**Bucket name** is globally unique. You need to add *-2ada* after it that your **Bucket name** matches [the bucket naming rules.](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html?icmpid=docs_amazons3_console)
{{% /notice %}} 
![iam-1](/images/2-Prerequiste/2.1-createbucket/s3-3.png)
4. Your bucket created successfully
![iam-1](/images/2-Prerequiste/2.1-createbucket/s3-4.png)