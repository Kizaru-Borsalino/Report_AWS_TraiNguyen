---
title: "Workshop"
date: 2026-08-05
weight: 5
chapter: false
pre: " <b> 5. </b> "
---


Phần này trình bày **project kỹ thuật chính** của báo cáo: triển khai nền tảng tuyển dụng **JobGo** trên AWS theo hướng end-to-end. Khác với workshop mẫu của FCAJ, nội dung bên dưới bám sát use case của chính dự án: website tìm việc có khách truy cập công khai, ứng viên, doanh nghiệp, quản trị viên và điểm nhấn là **AI Matching Engine**.

## Mục tiêu

- Phân phối frontend React qua **Amazon S3 + Amazon CloudFront**.
- Đóng gói backend FastAPI thành container và chạy trên **Amazon ECS Fargate** sau **Application Load Balancer**.
- Lưu dữ liệu quan hệ trong **Amazon RDS for PostgreSQL**.
- Lưu CV và tệp đính kèm vào **Amazon S3 private bucket**.
- Quan sát hệ thống bằng **Amazon CloudWatch Logs** và alarm cơ bản.
- Tái hiện cách điểm **AI Matching** được tính từ master data hồ sơ ứng viên và tin tuyển dụng.

## Nội dung workshop

1. [Tổng quan kiến trúc và bài toán triển khai](./5.1-Workshop-overview/)
2. [Điều kiện chuẩn bị](./5.2-Prerequiste/)
3. [Triển khai frontend với S3 và CloudFront](./5.3-S3-vpc/)
4. [Triển khai backend, cơ sở dữ liệu và AI matching](./5.4-S3-onprem/)
5. [Bảo mật, IAM, logging và validation](./5.5-Policy/)
6. [Dọn dẹp tài nguyên và bàn giao](./5.6-Cleanup/)
