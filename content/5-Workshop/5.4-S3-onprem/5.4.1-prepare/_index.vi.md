---
title: "Chuẩn bị VPC, RDS và private bucket"
date: 2026-08-08
weight: 1
chapter: false
pre: " <b> 5.4.1. </b> "
---

## Thành phần cần tạo

- 1 VPC với public subnet cho ALB và private subnet cho ECS/RDS.
- 1 security group cho ALB và 1 security group cho ECS.
- 1 [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html) cho dữ liệu nghiệp vụ.
- 1 private bucket `jobgo-resume-prod` cho CV và file đính kèm.

## Lưu ý thiết kế

- ALB nhận request từ Internet, còn ECS task chỉ nhận traffic từ ALB.
- RDS chỉ cho phép inbound từ security group của ECS.
- Bucket CV không public; backend tạo pre-signed URL hoặc stream file theo phân quyền.

## Các bảng dữ liệu chính

- `users`, `student_profiles`, `company_profiles`
- `jobs`, `applications`, `resumes`
- `skills`, `job_positions`, `levels`, `locations`, `employment_types`, `work_modes`

Thiết kế này giúp AI matching không phải so sánh text tự do mà dựa trên master data chuẩn hóa.
