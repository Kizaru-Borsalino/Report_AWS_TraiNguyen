---
title: "Build frontend v? upload l?n S3"
date: 2026-08-06
weight: 1
chapter: false
pre: " <b> 5.3.1. </b> "
---

## B??c 1: c?u h?nh bi?n m?i tr??ng build

```env
VITE_API_BASE_URL=https://api.jobgo.example.com
```

## B??c 2: build frontend

```bash
cd frontend
npm ci
npm run build
```

K?t qu? s? t?o th? m?c `dist/` ch?a HTML, CSS, JavaScript v? static assets.

## B??c 3: t?o bucket frontend

```bash
aws s3 mb s3://jobgo-frontend-prod --region ap-southeast-1
aws s3 sync dist s3://jobgo-frontend-prod --delete
```

## B??c 4: l?u ? tri?n khai

- N?u d?ng [Origin Access Control](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html), bucket kh?ng c?n public.
- V?i SPA React, c?n c?u h?nh CloudFront ho?c error response ?? m?i route ch?a c? file v?t l? ??u tr? v? `index.html`.
- Sau m?i l?n release, ch? c?n build l?i `dist/` v? sync ?? l?n bucket.
