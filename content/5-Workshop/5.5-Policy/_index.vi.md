---
title: "Bảo mật, IAM, logging và validation"
date: 2026-08-11
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

## IAM và nguyên tắc quyền hạn tối thiểu

- ECS task role chỉ được quyền `s3:GetObject`, `s3:PutObject` trên bucket CV.
- Tài khoản build/release mới có quyền push image lên ECR và cập nhật ECS service.
- Không hard-code access key trong source; bí mật nên đặt trong [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) hoặc [AWS Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html).

## Bảo mật tầng mạng

- Chỉ ALB public; ECS và RDS đặt trong private subnet.
- Security group của RDS chỉ mở cổng PostgreSQL cho security group của ECS.
- Bucket CV giữ private hoàn toàn; frontend không truy cập trực tiếp.

## CORS và upload file

- `CORS_ORIGINS` chỉ cho phép domain frontend của JobGo.
- Backend kiểm tra loại file, kích thước file và quyền truy cập trước khi cho tải hoặc xem CV.

## Logging và cảnh báo

- Gửi log ứng dụng vào CloudWatch Logs theo từng ECS task.
- Tạo alarm cho 5xx ở ALB, CPU/Memory bất thường ở ECS và tình trạng kết nối RDS.
- Ghi lại các event quan trọng: đăng nhập, tạo tin, ứng tuyển, thay đổi trạng thái ứng tuyển.
