---
title : "Giới Thiệu"
date : "`r Sys.Date()`"
weight : 1
chapter : false
pre : "<b> 1. </b>"
---

### Amazon S3
**Amazon Simple Storage Service (Amazon S3)** là một dịch vụ lưu trữ đối tượng với khả năng mở rộng hàng đầu, tính sẵn sàng cao, bảo mật và hiệu suất tối ưu. Amazon S3 được thiết kế để cung cấp lưu trữ dung lượng lớn, chi phí thấp trên nhiều khu vực địa lý.
### Amazon SNS
**Amazon Simple Notification Service (Amazon SNS)** là một dịch vụ web quản lý việc gửi hoặc nhận tin nhắn tới các đầu cuối hoặc máy khách đăng ký.
### Amazon SQS
**Amazon Simple Queue Service (Amazon SQS)** cung cấp một hàng đợi an toàn, bền bỉ và khả dụng, cho phép gửi, lưu trữ và nhận tin nhắn giữa các thành phần phần mềm với bất kỳ khối lượng nào mà không mất tin nhắn.
### AWS Lambda
**AWS Lambda** là một dịch vụ tính toán thực thi mã của bạn để đáp ứng các sự kiện và tự động quản lý tài nguyên tính toán.
### Lợi Ích Của Kiến Trúc Này:
- **Khả năng mở rộng:** Các thành phần serverless tự động mở rộng để đáp ứng khối lượng công việc thay đổi.
- **Giảm liên kết chặt chẽ:** SNS và SQS giúp các thành phần linh hoạt và dễ bảo trì hơn.
- **Độ tin cậy:** SQS đảm bảo việc giao tin nhắn đáng tin cậy với cơ chế thử lại.
- **Chi phí hiệu quả :** Các dịch vụ serverless như S3 và Lambda chỉ tính phí dựa trên sử dụng.