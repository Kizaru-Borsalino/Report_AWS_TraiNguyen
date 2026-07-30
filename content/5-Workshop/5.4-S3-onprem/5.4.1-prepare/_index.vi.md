---
title : "Chuẩn bị EC2 và RDS"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.4.1. </b> "
---

## RDS PostgreSQL

Tạo database production với thông tin đề xuất:

```text
Engine: PostgreSQL
DB name: internship_portal
Username: app_user
Public access: No
Storage: 20 GB
```

Security group của RDS chỉ mở port `5432` cho security group của EC2 backend.

## EC2 backend

Tạo EC2 instance dùng Ubuntu LTS. Cấu hình inbound rule:

```text
22: từ IP cá nhân để SSH
80/443: từ internet nếu dùng Nginx/HTTPS
8000: chỉ mở tạm thời trong giai đoạn test
```

Sau khi tạo EC2, gắn IAM Role có quyền tối thiểu với S3 bucket CV.

## Kết quả

Môi trường cloud đã có server backend, database riêng và network rule đủ để backend kết nối RDS.
