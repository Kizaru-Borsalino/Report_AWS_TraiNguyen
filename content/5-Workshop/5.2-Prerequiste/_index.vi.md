---
title : "Chuẩn bị môi trường AWS"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.2. </b> "
---

## 1. Chọn Region

Dự án ưu tiên triển khai tại region:

```text
ap-southeast-1
```

Việc dùng một region duy nhất giúp giảm độ phức tạp khi cấu hình EC2, RDS, S3, IAM và CloudWatch.

## 2. Chuẩn bị IAM

Cần tạo hoặc sử dụng IAM user/role có quyền thao tác các dịch vụ:

- EC2
- RDS
- S3
- IAM
- CloudWatch

Khi deploy production, nên gắn **IAM Role** vào EC2 thay vì lưu access key trực tiếp trong file `.env`.

## 3. Chuẩn bị backend environment

Backend cần các biến môi trường chính:

```env
DATABASE_URL=postgresql+psycopg2://app_user:<password>@<rds-endpoint>:5432/internship_portal
AWS_REGION=ap-southeast-1
S3_BUCKET_NAME=<your-cv-bucket>
S3_PRESIGNED_URL_EXPIRE_SECONDS=300
BACKEND_CORS_ORIGINS=https://your-frontend-domain.com
REFRESH_COOKIE_SECURE=true
REFRESH_COOKIE_SAMESITE=none
```

## 4. Chuẩn bị frontend environment

Frontend cần trỏ tới API production:

```env
VITE_API_URL=https://your-api-domain.com
```

Sau đó build bằng:

```powershell
cd frontend
npm.cmd install
npm.cmd run build
```
