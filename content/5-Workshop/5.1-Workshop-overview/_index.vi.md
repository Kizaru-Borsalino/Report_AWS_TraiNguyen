---
title : "Tổng quan kiến trúc"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

Workshop triển khai dự án **Student Internship Portal** trên AWS theo mô hình web application nhiều thành phần.

## Thành phần chính

```text
Browser
  -> Frontend React on S3/CloudFront
  -> FastAPI Backend on EC2
  -> Amazon RDS PostgreSQL
  -> Amazon S3 private bucket for CV files
  -> Amazon CloudWatch Logs
```
## Kiến trúc dự án
![Ảnh kiến trúc dự án](/images/cloud_aws_architec.png)

## Vai trò của từng dịch vụ

- **Amazon EC2:** chạy backend FastAPI bằng Uvicorn.
- **Amazon RDS PostgreSQL:** lưu dữ liệu nghiệp vụ như user, profile, company, internship post, application, skills, notification và forum.
- **Amazon S3:** lưu file CV trong private bucket và có thể host frontend static build.
- **Amazon CloudFront:** phân phối frontend qua HTTPS và cải thiện tốc độ truy cập.
- **IAM Role:** cấp quyền tối thiểu cho backend truy cập S3.
- **Security Group:** kiểm soát traffic vào EC2 và RDS.
- **CloudWatch Logs:** thu thập log backend để kiểm tra lỗi và theo dõi vận hành.

## Luồng xử lý upload CV

1. Student upload CV từ frontend.
2. Frontend gửi request tới FastAPI backend.
3. Backend kiểm tra quyền, định dạng và kích thước file.
4. Backend upload file lên S3 private bucket.
5. Database lưu object key của file.
6. Khi company cần xem CV, backend tạo presigned URL tạm thời nếu company có quyền xem hồ sơ đó.

