---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

Workshop tập trung vào các kỹ thuật cloud chính được sử dụng để đưa dự án từ môi trường local lên AWS. Nội dung bám theo bài toán: xây dựng một cổng thông tin thực tập có backend, frontend, database, lưu trữ CV riêng tư và logging cơ bản.

## Mục tiêu

- Deploy backend FastAPI lên Amazon EC2.
- Sử dụng Amazon RDS PostgreSQL thay cho SQLite local.
- Lưu file CV trên Amazon S3 private bucket.
- Build frontend React và deploy lên S3 Static Website Hosting hoặc CloudFront.
- Cấu hình IAM, Security Group, CORS và biến môi trường production.
- Theo dõi log backend bằng Amazon CloudWatch Logs.

## Nội dung workshop

1. [Tổng quan kiến trúc triển khai](5.1-Workshop-overview/)
2. [Chuẩn bị môi trường AWS](5.2-Prerequiste/)
3. [Cấu hình S3 lưu trữ CV](5.3-S3-vpc/)
4. [Triển khai backend và database](5.4-S3-onprem/)
5. [IAM, bảo mật và CORS production](5.5-Policy/)
6. [Kiểm thử, giám sát và dọn dẹp tài nguyên](5.6-Cleanup/)

## Kiến trúc triển khai

```text
Browser
  -> S3 Static Website Hosting or CloudFront
  -> React frontend
  -> EC2 FastAPI backend
  -> RDS PostgreSQL
  -> S3 private bucket for CV files
  -> CloudWatch Logs
```
