+++
title = "Check logs in CloudWatch Logs"
date = 2022
weight = 9
chapter = false
pre = "<b>8.2 </b>"
+++
In this check result section, I will upload a new file to the bucket and copy file. Then, I will check log in **CloudWatch Log**.

1. In the **AWS Management Console**. Enter and select **ClouwWatch** in search bar
![iam-1](/images/8-checkresult/8.2-checklog/check-1.png)
2. In the left panel, expand **Logs** choose **Log groups** and **/aws/lambda/lambda1** log group
![iam-1](/images/8-checkresult/8.2-checklog/check-2.png)
3. In the **Log group** detail. Scroll down and choose **Log stream**
![iam-1](/images/8-checkresult/8.2-checklog/check-3.png)
4. A file is uploaded or copied to the bucket **mybucket-2ada**. S3 fires the event. S3 sends a notification to the SNS topic **myTopic**. The notification contains event information (bucket name, file, time, etc.). SNS forwards the notification to the SQS queue **queue1**. Lambda can process this notification from SQS.
![iam-1](/images/8-checkresult/8.2-checklog/check-4.png)
5. Go to **mybucket-2ada** details:
    - Choose the file
    - Choose **Actions** to expand and choose **Copy**
![iam-1](/images/8-checkresult/8.2-checklog/check-5.png)
6. In the **Copy** details. Destination: `s3://mybucket-2ada/new/` and choose **Copy**
![iam-1](/images/8-checkresult/8.2-checklog/check-6.png)
7. Come back to **Log groups** in **CloudWatch Log** interface 
    - Choose **/aws/lambda/lambda2** log group
    - Choose **Log stream**
![iam-1](/images/8-checkresult/8.2-checklog/check-7.png)
![iam-1](/images/8-checkresult/8.2-checklog/check-8.png)
![iam-1](/images/8-checkresult/8.2-checklog/check-9.png)

