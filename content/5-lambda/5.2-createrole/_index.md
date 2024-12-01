+++
title = "Create a role"
date = 2022
weight = 5
chapter = false
pre = "<b>5.2 </b>"
+++
1. In the **AWS Management Console**. Enter and select **IAM** in search bar
![search](/images/5-lambda/5.1-createpolicy/policy-1.png)
2. In the left panel, choose **Role** and select **Create role**
![search](/images/5-lambda/5.2-createrole/role-1.png)
3. In the **Create role** details:
    - **Trusted entity type:** AWS service
    - **Service or use case**: Lambda
    - Choose **Next**
![search](/images/5-lambda/5.2-createrole/role-2.png)
4. Next step, you need to find and choose the policy **LambdaPolicy1**
![search](/images/5-lambda/5.2-createrole/role-3.png)
5. In the role details:
    - **Role name:** `LambdaRole1                 `
    - Choose **Create role**
![search](/images/5-lambda/5.2-createrole/role-4.png)
6. We continue create the second role. Choose the policy **LambdaPolicy2**
![search](/images/5-lambda/5.2-createrole/role-5.png)
    - **Role name:** `LambdaRole2                 `
    - Choose **Create role**
![search](/images/5-lambda/5.2-createrole/role-6.png)