---
title : "Tổng Quan"
date : "`r Sys.Date()`"
weight : 5
chapter : false
---
# Triển Khai Kiến Trúc Sự Kiện

### Tổng Quan
**Kiến trúc dựa trên sự kiện (Event-driven architecture - EDA)** là một mô hình kiến trúc hiện đại, được xây dựng từ các dịch vụ nhỏ, độc lập, hoạt động bằng cách xuất bản, tiêu thụ hoặc định tuyến sự kiện.

Khác với mô hình dựa trên yêu cầu truyền thống, EDA khuyến khích giảm sự liên kết chặt chẽ giữa các dịch vụ sản xuất và tiêu thụ, giúp dễ dàng mở rộng, cập nhật và triển khai độc lập các thành phần của hệ thống.

![Kết nối riêng tư](/images/architect.png)

### Nội Dung
1. [Giới Thiệu](1-Introduce/)
2. [Chuẩn Bị](2-Prerequiste/)
3. [Tạo Hàng Đợi SQS](3-sqs/)
4. [Tạo Chủ Đề SNS](4-sns/)
5. [Tạo Hàm Lambda](5-lambda/)
6. [Tạo Thông Báo Sự Kiện Trong S3](6-createnotis3/)
7. [Kích Hoạt Hàm Lambda Qua SQS](7-triggerlambda/)
8. [Kiểm Tra Kết Quả](8-checkresult/)
9. [Dọn Dẹp](9-cleanup/)