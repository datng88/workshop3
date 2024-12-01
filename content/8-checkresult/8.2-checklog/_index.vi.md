+++
title = "Kiểm tra nhật ký trong CloudWatch Logs"
date = 2022
weight = 9
chapter = false
pre = "<b>8.2 </b>"
+++

Trong phần kiểm tra kết quả này, bạn sẽ tải tệp mới lên bucket và sao chép tệp. Sau đó, kiểm tra nhật ký trong **CloudWatch Logs**.  
1. Trong **AWS Management Console**, nhập và chọn **CloudWatch** trong thanh tìm kiếm.  
![check-1](/images/8-checkresult/8.2-checklog/check-1.png)
2. Trong bảng điều khiển bên trái, mở rộng **Logs**, chọn **Log groups** và nhóm nhật ký **/aws/lambda/lambda1**.  
![check-2](/images/8-checkresult/8.2-checklog/check-2.png)
3. Trong chi tiết **Log group**, cuộn xuống và chọn **Log stream**.  
![check-3](/images/8-checkresult/8.2-checklog/check-3.png)
4. Khi một tệp được tải lên hoặc sao chép vào bucket **mybucket-2ada**, S3 kích hoạt sự kiện và gửi thông báo đến chủ đề SNS **myTopic**. Thông báo này chứa thông tin sự kiện (tên bucket, tệp, thời gian, v.v.). SNS chuyển tiếp thông báo đến hàng đợi SQS **queue1**. Lambda sẽ xử lý thông báo này từ SQS.  
![check-4](/images/8-checkresult/8.2-checklog/check-4.png)
5. Quay lại chi tiết bucket **mybucket-2ada**:  
   - Chọn tệp.  
   - Nhấn **Actions** để mở rộng và chọn **Copy**.  
![check-5](/images/8-checkresult/8.2-checklog/check-5.png)
1. Trong chi tiết **Copy**, chỉ định **Destination**: `s3://mybucket-2ada/new/` và nhấn **Copy**.  
![check-6](/images/8-checkresult/8.2-checklog/check-6.png)
1. Quay lại **Log groups** trong giao diện **CloudWatch Logs**:  
   - Chọn nhóm nhật ký **/aws/lambda/lambda2**.  
   - Chọn **Log stream** để xem chi tiết.  
![check-7](/images/8-checkresult/8.2-checklog/check-7.png)
![check-8](/images/8-checkresult/8.2-checklog/check-8.png)
![check-9](/images/8-checkresult/8.2-checklog/check-9.png)