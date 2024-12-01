+++
title = "Tạo vai trò"
date = 2022
weight = 5
chapter = false
pre = "<b>5.2 </b>"
+++
1. Trong **AWS Management Console**, nhập và chọn **IAM** từ thanh tìm kiếm  
![search](/images/5-lambda/5.1-createpolicy/policy-1.png)
2. Trong bảng điều khiển bên trái, chọn **Role** và nhấp **Create role**  
![search](/images/5-lambda/5.2-createrole/role-1.png)
3. Trong chi tiết **Create role**:
    - **Trusted entity type:** AWS service  
    - **Service or use case**: Lambda  
    - Chọn **Next**  
![search](/images/5-lambda/5.2-createrole/role-2.png)
4. Ở bước tiếp theo, tìm và chọn chính sách **LambdaPolicy1**  
![search](/images/5-lambda/5.2-createrole/role-3.png)
5. Trong chi tiết vai trò:
    - **Role name:** `LambdaRole1`  
    - Chọn **Create role**  
![search](/images/5-lambda/5.2-createrole/role-4.png)
6. Tiếp tục tạo vai trò thứ hai. Chọn chính sách **LambdaPolicy2**  
    - **Role name:** `LambdaRole2`  
    - Chọn **Create role**  
![search](/images/5-lambda/5.2-createrole/role-6.png)