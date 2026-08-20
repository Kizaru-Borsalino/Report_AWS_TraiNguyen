---
title: "C?u h?nh CloudFront v? ki?m th? frontend"
date: 2026-08-07
weight: 2
chapter: false
pre: " <b> 5.3.2. </b> "
---

## C?c c?u h?nh ch?nh

- T?o distribution v?i origin l? bucket `jobgo-frontend-prod`.
- B?t [Origin Access Control](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) ?? tr?nh public bucket.
- ??t `Default root object` l? `index.html`.
- C?u h?nh custom error response `403/404 -> /index.html` ?? h? tr? SPA routing.

## Invalidating cache sau khi ph?t h?nh

```bash
aws cloudfront create-invalidation   --distribution-id E1234567890   --paths "/*"
```

## K?t qu? c?n x?c nh?n

- Trang ch? hi?n th? danh s?ch vi?c l?m c?ng khai cho guest.
- N?t `??ng nh?p` m? form x?c th?c thay v? ch?n ng??i d?ng ch?a c? t?i kho?n.
- Frontend g?i ??ng API production qua `VITE_API_BASE_URL`.
- Route chi ti?t tin tuy?n d?ng ho?t ??ng khi ng??i d?ng refresh trang.
