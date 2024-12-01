+++
title = "Tạo thông báo sự kiện"
date = 2022
weight = 6
chapter = false
pre = "<b>6.1 </b>"
+++

1. Trong **AWS Management Console**, nhập và chọn **S3** trong thanh tìm kiếm.  
   ![s3-1](/images/2-Prerequiste/2.1-createbucket/s3-1.png)
2. Chọn bucket **mybucket-2ada**.  
   ![noti-1](/images/6-createnotis3/6.1-createeventnoti/noti-1.png)
3. Đi đến **Properties**, cuộn xuống gần cuối trang và chọn **Create event notification**.  
   ![noti-2](/images/6-createnotis3/6.1-createeventnoti/noti-2.png)
4. Trong giao diện **Create event notification**:  
   - **Tên sự kiện:** newObjectNotifier  
   - **Object creation:** All object create events  
   - **Destination**: SNS topic  
   - **Specify SNS topic:** Chọn từ các SNS topic của bạn.  
   - Nhấn **Save changes**.  
![noti-3](/images/6-createnotis3/6.1-createeventnoti/noti-3.png)