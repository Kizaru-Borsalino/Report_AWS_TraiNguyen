---
title: "Cấu hình CloudFront và kiểm thử frontend"
date: 2026-08-07
weight: 2
chapter: false
pre: " <b> 5.3.2. </b> "
---

## Các cấu hình chính

- Tạo distribution với origin là bucket `jobgo-frontend-prod`.
- Bật [Origin Access Control](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) để tránh public bucket.
- Đặt `Default root object` là `index.html`.
- Cấu hình custom error response `403/404 -> /index.html` để hỗ trợ SPA routing.

## Invalidating cache sau khi phát hành

```bash
aws cloudfront create-invalidation   --distribution-id E1234567890   --paths "/*"
```

## Kết quả cần xác nhận

- Trang chủ hiển thị danh sách việc làm công khai cho guest.
- Nút `Đăng nhập` mở form xác thực thay vì chặn người dùng chưa có tài khoản.
- Frontend gọi đúng API production qua `VITE_API_BASE_URL`.
- Route chi tiết tin tuyển dụng hoạt động khi người dùng refresh trang.
