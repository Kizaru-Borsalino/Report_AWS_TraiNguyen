---
title: "Điều kiện chuẩn bị"
date: 2026-08-05
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

## Điều kiện cần có

- Tài khoản AWS có quyền với S3, CloudFront, ECS, ECR, RDS, IAM và CloudWatch
- Docker để build image backend
- Node.js để build frontend
- AWS CLI để thao tác nhanh nếu cần
- Bộ biến môi trường production cho backend
- Dữ liệu seed cơ bản cho tài khoản, master data và role

## Đầu ra mong muốn

Sau khi hoàn thành workshop, người thực hiện có thể:

- truy cập giao diện JobGo qua CloudFront,
- gọi backend API qua ALB,
- xác minh backend đang kết nối được với RDS,
- tải CV lên private S3 bucket,
- xem log backend trên CloudWatch.
