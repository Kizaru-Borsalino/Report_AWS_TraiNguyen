---
title: "Tổng quan workshop"
date: 2026-08-05
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

## Bối cảnh

JobGo là một nền tảng tuyển dụng nhiều vai trò gồm guest, ứng viên, doanh nghiệp và quản trị viên. Bài toán không chỉ dừng ở việc hiển thị giao diện hay CRUD dữ liệu, mà còn cần:

- phân phối frontend hiệu quả,
- chạy backend API ổn định,
- lưu CV an toàn,
- tách dữ liệu nghiệp vụ ra khỏi file storage,
- theo dõi hệ thống sau khi triển khai.

## Mục tiêu workshop

Workshop này mô tả cách triển khai JobGo trên AWS theo mô hình production cơ bản:

- frontend React qua **Amazon S3 + CloudFront**,
- backend FastAPI qua **Amazon ECS Fargate + ALB**,
- dữ liệu quan hệ trên **Amazon RDS PostgreSQL**,
- CV trên **private S3 bucket**,
- logging và validation qua **Amazon CloudWatch**.

## Kiến trúc tổng quan

```text
User Browser
  -> CloudFront
  -> S3 static frontend
  -> Application Load Balancer
  -> ECS Fargate service (FastAPI backend)
  -> Amazon RDS PostgreSQL
  -> Amazon S3 private bucket (resume files)
  -> CloudWatch Logs / Alarms
```
