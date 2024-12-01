+++
title = "Clean up"
date = 2022
weight = 9
chapter = false
pre = "<b>9. </b>"
+++
1. Go to **Amazon S3** interface. Select **mybucket-2ada** bucket and **Empty** 
![iam-1](/images/9-cleanup/clean-1.png)
1. Type `permanently delete` to confirm deletion 
![iam-1](/images/9-cleanup/clean-2.png)
1. Go to **Amazon SNS** interface. In the left panel, choose **Topics** and choose **Delete** respectively
![iam-1](/images/9-cleanup/clean-3.png)
1. Type `delete me` to confirm deletion
![iam-1](/images/9-cleanup/clean-4.png)
1. Go to **Amazon SQS** interface. Select **queue1** and choose **Delete**
![iam-1](/images/9-cleanup/clean-5.png)
1. Type `confirm             ` to agree
![iam-1](/images/9-cleanup/clean-6.png)
1. We continue choose **queue2** and **Delete**
![iam-1](/images/9-cleanup/clean-7.png)
1. Type `confirm             ` to agree
![iam-1](/images/9-cleanup/clean-8.png)
1. Go to **Lambda** interface. Choose both of function and choose **Delete**
![iam-1](/images/9-cleanup/clean-9.png)
1. Type `delete          ` to confirm deletion
![iam-1](/images/9-cleanup/clean-10.png)