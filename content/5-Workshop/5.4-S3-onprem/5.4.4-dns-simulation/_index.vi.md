---
title : "Deploy frontend"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4.4. </b> "
---

## Cấu hình API URL

Trong `frontend/.env`, cấu hình:

```env
VITE_API_URL=https://your-api-domain.com
```

Nếu chỉ test trực tiếp bằng public IP EC2:

```env
VITE_API_URL=http://<ec2-public-ip>:8000
```

## Build frontend

```powershell
cd frontend
npm.cmd install
npm.cmd run build
```

Kết quả build nằm trong thư mục `dist`.

## Upload lên S3

```powershell
aws s3 sync dist/ s3://<your-frontend-bucket> --delete
```

## Cấu hình hosting

Có hai hướng:

- **S3 Static Website Hosting:** phù hợp demo nhanh.
- **CloudFront + S3:** phù hợp production hơn vì hỗ trợ HTTPS, cache và phân phối tốt hơn.

## Kiểm thử

Mở frontend domain, đăng nhập thử bằng tài khoản demo và kiểm tra các trang student, company, admin có gọi được backend API không.
