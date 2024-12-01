+++
title = "Create a policy"
date = 2022
weight = 5
chapter = false
pre = "<b>5.1 </b>"
+++
1. In the **AWS Management Console**. Enter and select **IAM** in search bar
![search](/images/5-lambda/5.1-createpolicy/policy-1.png)
2. In the left panel, choose **Policies** and select **Create policy**
![search](/images/5-lambda/5.1-createpolicy/policy-2.png)
3. In **Create policy** details:
    - **Policy editor:** JSON
    - Paste the following code and edit 
    - Choose **Next**
{{% notice note %}}
Check the replacement parameters such as region, accountId, snsTopicName, s3BucketName, snsTopicName, and sqsQueueName to ensure the code is properly configured for your AWS environment.
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
![search](/images/5-lambda/5.1-createpolicy/policy-4.png)
4. In the **Review and create** details:
    - **Policy name:** `LambdaPolicy1                    `
    - Choose **Create Policy**
![search](/images/5-lambda/5.1-createpolicy/policy-5.png)
5. We continue create the second policy. In **Create policy** details:
    - **Policy editor:** JSON
    - Reuse the old code and edit
    - Choose **Next**
![search](/images/5-lambda/5.1-createpolicy/policy-6.png)
6. In the **Review and create** details:
    - **Policy name:** `LambdaPolicy2                    `
    - Choose **Create Policy**
![search](/images/5-lambda/5.1-createpolicy/policy-7.png)
