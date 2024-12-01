+++
title = "Create a event notification"
date = 2022
weight = 6
chapter = false
pre = "<b>6.1 </b>"
+++
1. In the **AWS Management Console**. Enter and select **S3** in search bar
![iam-1](/images/2-Prerequiste/2.1-createbucket/s3-1.png)
2. Choose **mybucket-2ada** bucket
![iam-1](/images/6-createnotis3/6.1-createeventnoti/noti-1.png)
3. Go to **Properties**. Scroll down to near the end of page to choose **Create event notification**
![iam-1](/images/6-createnotis3/6.1-createeventnoti/noti-2.png)
4. In the **Create event notification** interface:
    - **Event name:** `newObjectNotifier         `
    - **Object creation:** All object create events
    - **Destination**: SNS topic
    - **Specify SNS topic:** Choose from your SNS topics
    - Choose **Save changes**
![iam-1](/images/6-createnotis3/6.1-createeventnoti/noti-3.png)
