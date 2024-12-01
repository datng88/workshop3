+++
title = "Tạo một chủ đề"
date = 2022
weight = 4
chapter = false
pre = "<b>4.1 </b>"
+++

1. Trong **AWS Management Console**, nhập và chọn **SNS** trong thanh tìm kiếm.  
![dynamodb-1](/images/4-sns/4.1-createtopic/sns-1.png)

1. Trong bảng điều khiển bên trái, chọn **Topics** và sau đó chọn **Create topic**.  
   - Trong phần chi tiết **Create topic**:
     - **Type:** Standard
     - **Name:** `myTopic`
     - **Access policy - optional:** Advanced
     - Xóa, dán đoạn mã sau.
{{% notice note %}}
Check the replacement parameters such as region, accountId, snsTopicName, s3BucketName, snsTopicName, and sqsQueueName to ensure the code is properly configured for your AWS environment.
{{% /notice %}}
```json
{
  "Version": "2008-10-17",
  "Id": "__default_policy_ID",
  "Statement": [
    {
      "Sid": "__default_statement_ID",
      "Effect": "Allow",
      "Principal": {
        "Service": "s3.amazonaws.com"
      },
      "Action": "SNS:Publish",
      "Resource": "arn:aws:sns:<region>:<accountId>:<snsTopicName>",
      "Condition": {
        "StringEquals": {
          "aws:SourceAccount": "<accountId>"
        },
        "ArnLike": {
          "aws:SourceArn": "arn:aws:s3:*:*:<s3BucketName>"
        }
      }
    },
    {
      "Sid": "sqs_statement",
      "Effect": "Allow",
      "Principal": {
        "Service": "sqs.amazonaws.com"
      },
      "Action": "sns:Subscribe",
      "Resource": "arn:aws:sns:<region>:<accountId>:<snsTopicName>",
      "Condition": {
        "ArnEquals": {
          "aws:SourceArn": [
            "arn:aws:sqs:<region>:<accountId>:<sqsQueueName>",
            "arn:aws:sqs:<region>:<accountId>:<sqsQueueName>"
          ]
        }
      }
    }
  ]
}
```
![dynamodb-1](/images/4-sns/4.1-createtopic/sns-2.png)