---
title: "Workshop"
date: 2026-08-05
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Workshop

Ph?n n?y tr?nh b?y **project k? thu?t ch?nh** c?a b?o c?o: tri?n khai n?n t?ng tuy?n d?ng **JobGo** tr?n AWS theo h??ng end-to-end. Kh?c v?i workshop m?u c?a FCAJ, n?i dung b?n d??i b?m s?t use case c?a ch?nh d? ?n: website t?m vi?c c? kh?ch truy c?p c?ng khai, ?ng vi?n, doanh nghi?p, qu?n tr? vi?n v? ?i?m nh?n l? **AI Matching Engine**.

## M?c ti?u

- Ph?n ph?i frontend React qua **Amazon S3 + Amazon CloudFront**.
- ??ng g?i backend FastAPI th?nh container v? ch?y tr?n **Amazon ECS Fargate** sau **Application Load Balancer**.
- L?u d? li?u quan h? trong **Amazon RDS for PostgreSQL**.
- L?u CV v? t?p ??nh k?m v?o **Amazon S3 private bucket**.
- Quan s?t h? th?ng b?ng **Amazon CloudWatch Logs** v? alarm c? b?n.
- T?i hi?n c?ch ?i?m **AI Matching** ???c t?nh t? master data h? s? ?ng vi?n v? tin tuy?n d?ng.

## N?i dung workshop

1. [T?ng quan ki?n tr?c v? b?i to?n tri?n khai](./5.1-Workshop-overview/)
2. [?i?u ki?n chu?n b?](./5.2-Prerequiste/)
3. [Tri?n khai frontend v?i S3 v? CloudFront](./5.3-S3-vpc/)
4. [Tri?n khai backend, c? s? d? li?u v? AI matching](./5.4-S3-onprem/)
5. [B?o m?t, IAM, logging v? validation](./5.5-Policy/)
6. [D?n d?p t?i nguy?n v? b?n giao](./5.6-Cleanup/)
