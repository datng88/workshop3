+++
title = "Dọn dẹp"
date = 2022
weight = 9
chapter = false
pre = "<b>9. </b>"
+++

1. Truy cập giao diện **Amazon S3**. Chọn bucket **mybucket-2ada** và chọn **Empty**.  
   ![clean-1](/images/9-cleanup/clean-1.png)

2. Nhập `permanently delete` để xác nhận xóa.  
   ![clean-2](/images/9-cleanup/clean-2.png)

3. Truy cập giao diện **Amazon SNS**. Trong bảng điều khiển bên trái, chọn **Topics** và lần lượt chọn **Delete** cho từng chủ đề.  
   ![clean-3](/images/9-cleanup/clean-3.png)

4. Nhập `delete me` để xác nhận xóa.  
   ![clean-4](/images/9-cleanup/clean-4.png)

5. Truy cập giao diện **Amazon SQS**. Chọn **queue1** và chọn **Delete**.  
   ![clean-5](/images/9-cleanup/clean-5.png)

6. Nhập `confirm             ` để xác nhận đồng ý.  
   ![clean-6](/images/9-cleanup/clean-6.png)

7. Tiếp tục chọn **queue2** và chọn **Delete**.  
   ![clean-7](/images/9-cleanup/clean-7.png)

8. Nhập `confirm             ` để xác nhận đồng ý.  
   ![clean-8](/images/9-cleanup/clean-8.png)

9. Truy cập giao diện **Lambda**. Chọn cả hai hàm và chọn **Delete**.  
   ![clean-9](/images/9-cleanup/clean-9.png)

10. Nhập `delete          ` để xác nhận xóa.  
    ![clean-10](/images/9-cleanup/clean-10.png)
