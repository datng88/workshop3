+++
title = "Create a function"
date = 2022
weight = 6
chapter = false
pre = "<b>5.3 </b>"
+++
1. In the **AWS Management Console**. Enter and select **Lambda** in search bar
![search](/images/5-lambda/5.3-createfunc/func-1.png)
2. Choose **Create a function**
![search](/images/5-lambda/5.3-createfunc/func-2.png)
3. In the **Create funciton** detail:
    - **Type:** Author from scratch
    - **Function name:** `lambda1                `
    - **Runtime:** Python 3.8
    - **Execution role:** Use an existing role (LambdaRole1)
![search](/images/5-lambda/5.3-createfunc/func-3.png)
4. Replace this code *# TODO implement* with `print(json.dumps(event))`. Then, chooe **Deploy**
![search](/images/5-lambda/5.3-createfunc/func-5.png)
5. We continue create the second Lambda function:
    - **Type:** Author from scratch
    - **Function name:** `lambda2                `
    - **Runtime:** Python 3.8
    - **Execution role:** Use an existing role (LambdaRole2)
![search](/images/5-lambda/5.3-createfunc/func-4.png)
6. Replace this code *# TODO implement* with `print(json.dumps(event))`. Then, chooe **Deploy**
![search](/images/5-lambda/5.3-createfunc/func-6.png)

