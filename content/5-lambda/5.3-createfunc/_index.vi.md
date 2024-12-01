+++
title = "Tạo hàm"
date = 2022
weight = 6
chapter = false
pre = "<b>5.3 </b>"
+++

1. Trong **AWS Management Console**, nhập và chọn **Lambda** từ thanh tìm kiếm  
![search](/images/5-lambda/5.3-createfunc/func-1.png)
2. Chọn **Create a function**  
![search](/images/5-lambda/5.3-createfunc/func-2.png)
3. Trong chi tiết **Create function**:
    - **Type:** Author from scratch  
    - **Function name:** `lambda1`  
    - **Runtime:** Python 3.8  
    - **Execution role:** Sử dụng vai trò hiện có (LambdaRole1)  
![search](/images/5-lambda/5.3-createfunc/func-3.png)
4. Thay thế dòng *# TODO implement* bằng `print(json.dumps(event))`. Sau đó, chọn **Deploy**  
![search](/images/5-lambda/5.3-createfunc/func-5.png)
5. Tiếp tục tạo hàm Lambda thứ hai:
    - **Type:** Author from scratch  
    - **Function name:** `lambda2`  
    - **Runtime:** Python 3.8  
    - **Execution role:** Sử dụng vai trò hiện có (LambdaRole2)  
![search](/images/5-lambda/5.3-createfunc/func-4.png)
6. Thay thế dòng *# TODO implement* bằng `print(json.dumps(event))`. Sau đó, chọn **Deploy**  
![search](/images/5-lambda/5.3-createfunc/func-6.png)