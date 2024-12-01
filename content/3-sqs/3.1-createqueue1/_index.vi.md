---

title: "Tạo hàng đợi"
date: "r Sys.Date()"
weight: 3
chapter: false
pre: "<b> 3.1 </b>"
---
1. Trong **AWS Management Console**, nhập và chọn **SQS** trong thanh tìm kiếm
![iam-1](/images/3-sqs/3.1-createqueue1/queue-1.png)
2. Chọn **Create queue**
![iam-1](/images/3-sqs/3.1-createqueue1/queue-2.png)
3. Trong chi tiết **Create queue**:
    - **Type:** Standard
    - **Name**: `queue1                             `
    - **Access Policy:** Advanced method
    - Dán code sau và chỉnh sửa
    - Chọn **Create queue**
{{% notice note %}} Hãy kiểm tra các tham số thay thế như region, accountId, sqsQueueName, lambdaName, snsTopicName để đảm bảo mã được cấu hình đúng với môi trường AWS của bạn.
{{% /notice %}}

```json
{
  "Version": "2008-10-17",
  "Id": "__default_policy_ID",
  "Statement": [
    {
      "Sid": "Stmt1234",
      "Effect": "Allow",
      "Principal": {
        "Service": "lambda.amazonaws.com"
      },
      "Action": [
        "sqs:ReceiveMessage",
        "sqs:sendMessage"
      ],
      "Resource": "arn:aws:sqs:<region>:<accountId>:<sqsQueueName>",
      "Condition": {
        "ArnEquals": {
          "aws:SourceArn": "arn:aws:lambda:<region>:<accountId>:<lambdaName>"
        }
      }
    },
    {
      "Sid": "Stmt12345",
      "Effect": "Allow",
      "Principal": {
        "AWS": "*"
      },
      "Action": "sqs:SendMessage",
      "Resource": "arn:aws:sqs:<region>:<accountId>:<sqsQueueName>",
      "Condition": {
        "ArnLike": {
          "aws:SourceArn": "arn:aws:sns:<region>:<accountId>:<snsTopicName>"
        }
      }
    }
  ]
}
```
![iam-1](/images/3-sqs/3.1-createqueue1/queue-3.png)
4. Tiếp tục tạo hàng đợi thứ hai. Trong chi tiết **Create queue**:
  - **Type:** Standard
  - **Name**: `queue2                             `
  - **Access Policy:** Advanced method
  - Tái sử dụng đoạn mã cũ và chỉnh sửa.
  - Chọn **Create queue**
{{% notice note %}} Hãy kiểm tra các tham số thay thế như region, accountId, sqsQueueName, lambdaName, snsTopicName để đảm bảo mã được cấu hình đúng với môi trường AWS của bạn.
{{% /notice %}}
![iam-1](/images/3-sqs/3.1-createqueue1/queue-4.png)