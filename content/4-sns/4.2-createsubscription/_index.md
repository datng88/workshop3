+++
title = "Create subscription"
date = 2022
weight = 4
chapter = false
pre = "<b>4.2 </b>"
+++
1. Go to **Subscription** in the left panel and choose **Create subscription**
![dynamodb-1](/images/4-sns/4.2-createsubscription/sub-1.png)
2. In the **Create subscription** interface:
    - **Topic ARN:** myTopic
    - **Protocol:** Amazon SQS
    - **Endpoint:** queue1
    - Enable Subscription filter policy
    - **Filter policy scope:** Message body `json{"Records": {"eventName": ["ObjectCreated:Put"]} `
    - Choose **Create subscription**
![dynamodb-1](/images/4-sns/4.2-createsubscription/sub-2.png)
3. We continue create the second subscription for **queue2**
    - **Topic ARN:** myTopic
    - **Protocol:** Amazon SQS
    - **Endpoint:** queue2
    - Enable Subscription filter policy
    - **Filter policy scope:** Message body `json{"Records": {"eventName": ["ObjectCreated:Copy"]} `
    - Choose **Create subscription**
![dynamodb-1](/images/4-sns/4.2-createsubscription/sub-3.png)