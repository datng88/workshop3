+++
title = "Create a topic"
date = 2022
weight = 4
chapter = false
pre = "<b>4.1 </b>"
+++

1. In the **AWS Management Console**. Enter and select **SNS** in search bar
![dynamodb-1](/images/4-sns/4.1-createtopic/sns-1.png)
2. In the left panel. Choose **Topics** and then choose **Create topic**
   - In **Create topic** details:
     - **Type:** Standard
     - **Name**: `myTopic                     `
     - **Access policy - optional:** Advanced
     - Delete and paste the following code.
{{% notice note %}}
Check the replacement parameters like region, accountId, snsTopicName, s3BucketName, snsTopicName and sqsQueueName to ensure the code is properly configured for your AWS environment.
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

  