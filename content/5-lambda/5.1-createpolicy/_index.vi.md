+++
title = "Tạo một chính sách"
date = 2022
weight = 5
chapter = false
pre = "<b>5.1 </b>"
+++
1. Trong **AWS Management Console**, nhập và chọn **IAM** trong thanh tìm kiếm.  
   ![policy-1](/images/5-lambda/5.1-createpolicy/policy-1.png)
2. Trong bảng điều khiển bên trái, chọn **Policies** và nhấn **Create policy**.  
   ![policy-2](/images/5-lambda/5.1-createpolicy/policy-2.png)
3. Trong chi tiết **Create policy**:  
   - **Policy editor:** JSON  
   - Dán đoạn mã sau và chỉnh sửa.
{{% notice note %}}
Kiểm tra các tham số thay thế như region, accountId, snsTopicName, s3BucketName, snsTopicName và sqsQueueName để đảm bảo mã được cấu hình đúng cho môi trường AWS của bạn.
{{% /notice %}}
     ```json
     {
       "Version": "2012-10-17",
       "Statement": [
         {
           "Sid": "VisualEditor0",
           "Effect": "Allow",
           "Action": [
             "sqs:DeleteMessage",
             "logs:CreateLogStream",
             "sqs:ReceiveMessage",
             "sqs:GetQueueAttributes",
             "logs:PutLogEvents"
           ],
           "Resource": [
             "arn:aws:sqs:<region>:<accountId>:<sqsQueueName>",
             "arn:aws:logs:<region>:<accountId>:log-group:/aws/lambda/<lambdaName>:*"
           ]
         },
         {
           "Sid": "VisualEditor1",
           "Effect": "Allow",
           "Action": [
             "sqs:ReceiveMessage",
             "logs:CreateLogGroup"
           ],
           "Resource": [
             "arn:aws:logs:<region>:<accountId>:*",
             "arn:aws:sqs:<region>:<accountId>:<sqsQueueName>"
           ]
         }
       ]
     }
     ``` 
![policy-4](/images/5-lambda/5.1-createpolicy/policy-4.png)
4. Trong chi tiết **Review and create**:  
   - **Tên chính sách:** LambdaPolicy1  
   - Nhấn **Create Policy**.  
![policy-5](/images/5-lambda/5.1-createpolicy/policy-5.png)
5. Tiếp tục tạo chính sách thứ hai. Trong chi tiết **Create policy**:  
   - **Policy editor:** JSON  
   - Tái sử dụng đoạn mã cũ và chỉnh sửa.  
   - Nhấn **Next**. 
{{% notice note %}}
Kiểm tra các tham số thay thế như **<region>, <accountId>, <snsTopicName>, <s3BucketName>, <snsTopicName> và <sqsQueueName>** để đảm bảo mã được cấu hình đúng cho môi trường AWS của bạn.
{{% /notice %}}
![policy-6](/images/5-lambda/5.1-createpolicy/policy-6.png)
6. Trong chi tiết **Review and create**:  
   - **Policy name:** LambdaPolicy2  
   - Nhấn **Create Policy**.  
   ![policy-7](/images/5-lambda/5.1-createpolicy/policy-7.png)
