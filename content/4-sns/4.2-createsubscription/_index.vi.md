+++
title = "Tạo đăng ký"
date = 2022
weight = 4
chapter = false
pre = "<b>4.2 </b>"
+++
1. Đi đến **Subscription** trong bảng điều khiển bên trái và chọn **Create subscription**  
![dynamodb-1](/images/4-sns/4.2-createsubscription/sub-1.png)
2. Trong giao diện **Create subscription**:
    - **Topic ARN:** myTopic  
    - **Protocol:** Amazon SQS  
    - **Endpoint:** queue1  
    - Bật **Subscription filter policy**  
    - **Filter policy scope:** Message body `json{"Records": {"eventName": ["ObjectCreated:Put"]} `  
    - Chọn **Create subscription**  
![dynamodb-1](/images/4-sns/4.2-createsubscription/sub-2.png)
3. Tiếp tục tạo đăng ký thứ hai cho **queue2**:  
    - **Topic ARN:** myTopic  
    - **Protocol:** Amazon SQS  
    - **Endpoint:** queue2  
    - Bật **Subscription filter policy**  
    - **Filter policy scope:** Message body `json{"Records": {"eventName": ["ObjectCreated:Copy"]} `  
    - Chọn **Create subscription**  
![dynamodb-1](/images/4-sns/4.2-createsubscription/sub-3.png)