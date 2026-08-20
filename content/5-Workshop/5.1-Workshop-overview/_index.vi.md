---
title: "Tổng quan kiến trúc triển khai"
date: 2026-08-05
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

## Bối cảnh

JobGo là cổng tuyển dụng dành cho sinh viên và doanh nghiệp. Hệ thống cho phép:

- khách truy cập xem việc làm công khai,
- ứng viên tạo hồ sơ, quản lý CV, ứng tuyển và theo dõi lịch sử ứng tuyển,
- doanh nghiệp quản lý hồ sơ công ty, tạo tin tuyển dụng, xem danh sách ứng viên,
- quản trị viên duyệt nội dung, quản lý master data và giám sát hệ thống.

Điểm khác biệt của JobGo là **AI Matching Engine**: khi ứng viên cập nhật hồ sơ hoặc khi doanh nghiệp mở danh sách ứng viên, hệ thống tính mức độ phù hợp dựa trên kỹ năng, vị trí, cấp bậc, loại hình, hình thức làm việc và địa điểm.

## Mục tiêu kỹ thuật

- Tách frontend, backend, database và file storage để dễ vận hành.
- Không lưu CV công khai; mọi file ứng viên phải đi qua backend có kiểm soát quyền.
- Đảm bảo điểm matching có thể cập nhật lại khi hồ sơ ứng viên thay đổi.
- Chuẩn bị kiến trúc có thể mở rộng tiếp sang domain riêng, CI/CD và autoscaling.

## Kiến trúc triển khai

```text
Người dùng
  -> Amazon CloudFront
  -> Amazon S3 (frontend React build)
  -> Application Load Balancer
  -> Amazon ECS Fargate (FastAPI backend)
  -> Amazon RDS for PostgreSQL
  -> Amazon S3 private bucket (CV và file đính kèm)
  -> Amazon CloudWatch Logs / Alarms
```

## Lý do chọn dịch vụ

- [Amazon CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html): phân phối frontend nhanh, cache tốt và hỗ trợ HTTPS.
- [Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html): lưu static frontend và private resume storage chi phí thấp.
- [Amazon ECS Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html): chạy backend container mà không phải quản lý EC2.
- [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html): phù hợp với dữ liệu quan hệ của user, profile, job, application và master data.
- [Amazon CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html): thu log, theo dõi lỗi và cảnh báo 5xx cơ bản.

## Luồng triển khai

1. Build frontend từ mã nguồn React/Vite và publish lên S3.
2. Cấu hình CloudFront để phân phối giao diện và trỏ API về ALB.
3. Build backend FastAPI thành Docker image, đẩy lên ECR và chạy bằng ECS Fargate.
4. Kết nối backend đến RDS PostgreSQL và bucket private chứa CV.
5. Kiểm tra AI matching, upload CV, ứng tuyển và duyệt tin theo luồng end-to-end.
