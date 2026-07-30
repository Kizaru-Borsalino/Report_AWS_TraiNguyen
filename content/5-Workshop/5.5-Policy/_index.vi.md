---
title : "IAM, bảo mật và CORS"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

## IAM

Backend cần quyền truy cập S3 để upload và đọc CV. Trong production, hướng triển khai tốt hơn là gắn IAM Role cho EC2 thay vì lưu access key trong `.env`.

Nguyên tắc áp dụng:

- Chỉ cấp quyền `s3:PutObject` và `s3:GetObject` trên bucket CV.
- Không public bucket chứa CV.
- Không cấp quyền quản trị rộng cho backend.

## Security Group

Security group cần tách rõ:

- EC2 backend nhận request từ frontend/API gateway hoặc Nginx.
- RDS chỉ nhận kết nối từ EC2 backend.
- Port `8000` chỉ nên mở tạm khi test, sau đó dùng Nginx hoặc HTTPS endpoint.

## CORS production

Backend chỉ nên cho phép domain frontend thật:

```env
BACKEND_CORS_ORIGINS=https://your-frontend-domain.com
BACKEND_CORS_ORIGIN_REGEX=
REFRESH_COOKIE_SECURE=true
REFRESH_COOKIE_SAMESITE=none
```

Không nên dùng wildcard CORS trong production vì có thể làm tăng rủi ro truy cập API từ origin không mong muốn.

## Bảo vệ CV

CV được bảo vệ bằng ba lớp:

1. Bucket S3 private.
2. Backend kiểm tra quyền trước khi tạo link.
3. Presigned URL có thời hạn ngắn, ví dụ 300 giây.
