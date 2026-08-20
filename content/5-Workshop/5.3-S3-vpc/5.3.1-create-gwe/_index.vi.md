---
title: "Build frontend và upload lên S3"
date: 2026-08-06
weight: 1
chapter: false
pre: " <b> 5.3.1. </b> "
---

## Bước 1: cấu hình biến môi trường build

```env
VITE_API_BASE_URL=https://api.jobgo.example.com
```

## Bước 2: build frontend

```bash
cd frontend
npm ci
npm run build
```

Kết quả sẽ tạo thư mục `dist/` chứa HTML, CSS, JavaScript và static assets.

## Bước 3: tạo bucket frontend

```bash
aws s3 mb s3://jobgo-frontend-prod --region ap-southeast-1
aws s3 sync dist s3://jobgo-frontend-prod --delete
```

## Bước 4: lưu ý triển khai

- Nếu dùng [Origin Access Control](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html), bucket không cần public.
- Với SPA React, cần cấu hình CloudFront hoặc error response để mọi route chưa có file vật lý đều trả về `index.html`.
- Sau mỗi lần release, chỉ cần build lại `dist/` và sync đè lên bucket.
