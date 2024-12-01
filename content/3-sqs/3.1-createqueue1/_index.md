---
title : "Create a queue"
date : "`r Sys.Date()`"
weight : 3
chapter : false
pre : " <b> 3.1 </b> "
---
1. In the **AWS Management Console**. Enter and select **SQS** in search bar
![iam-1](/images/3-sqs/3.1-createqueue1/queue-1.png)
2. Choose **Create queue**
![iam-1](/images/3-sqs/3.1-createqueue1/queue-2.png)
3. In **Create queue** details:
    - **Type:** Standard
    - **Name**: `queue1                             `
    - **Access Policy:** Advanced method
    - Paste the following code and edit
    - Choose **Create queue**
{{% notice note %}}
Check the replacement parameters like region, accountId, snsTopicName, and s3BucketName to ensure the code is properly configured for your AWS environment.
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
4. We continue create the second queue. In **Create queue** details:
   - **Type:** Standard
   - **Name**: `queue2                             `
   - **Access Policy:** Advanced method
   - Reuse the old code and edit
   - Choose **Create queue**
![iam-1](/images/3-sqs/3.1-createqueue1/queue-4.png)

