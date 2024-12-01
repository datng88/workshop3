---
title : "Tạo Bucket"
date : "`r Sys.Date()`"
weight : 2
chapter : false
pre : "<b> 2.1 </b>"
---
1. Truy cập **AWS Management Console**. Tìm và chọn **S3** trong thanh tìm kiếm.
![Bước 1](/images/2-Prerequiste/2.1-createbucket/s3-1.png)
2. Chọn **Tạo Bucket**.
![Bước 2](/images/2-Prerequiste/2.1-createbucket/s3-2.png)
3. Trong chi tiết **Tạo Bucket**:
   - **Bucket name:** `myBucket`
   - **Bucket key:** Tắt
   - Chọn **Create Bucket**
{{% notice note %}}
**Bucket name** phải là duy nhất toàn cầu. Bạn cần thêm *-2ada* để phù hợp với [quy tắc đặt tên bucket.](https://docs.aws.amazon.com/AmazonS3/latest/userguide/bucketnamingrules.html?icmpid=docs_amazons3_console)
{{% /notice %}}
4. Bucket đã được tạo thành công.
![Thành công](/images/2-Prerequiste/2.1-createbucket/s3-4.png)
