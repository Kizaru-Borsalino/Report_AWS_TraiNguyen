---
title: "T?ng quan ki?n tr?c tri?n khai"
date: 2026-08-05
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

## B?i c?nh

JobGo l? c?ng tuy?n d?ng d?nh cho sinh vi?n v? doanh nghi?p. H? th?ng cho ph?p:

- kh?ch truy c?p xem vi?c l?m c?ng khai,
- ?ng vi?n t?o h? s?, qu?n l? CV, ?ng tuy?n v? theo d?i l?ch s? ?ng tuy?n,
- doanh nghi?p qu?n l? h? s? c?ng ty, t?o tin tuy?n d?ng, xem danh s?ch ?ng vi?n,
- qu?n tr? vi?n duy?t n?i dung, qu?n l? master data v? gi?m s?t h? th?ng.

?i?m kh?c bi?t c?a JobGo l? **AI Matching Engine**: khi ?ng vi?n c?p nh?t h? s? ho?c khi doanh nghi?p m? danh s?ch ?ng vi?n, h? th?ng t?nh m?c ?? ph? h?p d?a tr?n k? n?ng, v? tr?, c?p b?c, lo?i h?nh, h?nh th?c l?m vi?c v? ??a ?i?m.

## M?c ti?u k? thu?t

- T?ch frontend, backend, database v? file storage ?? d? v?n h?nh.
- Kh?ng l?u CV c?ng khai; m?i file ?ng vi?n ph?i ?i qua backend c? ki?m so?t quy?n.
- ??m b?o ?i?m matching c? th? c?p nh?t l?i khi h? s? ?ng vi?n thay ??i.
- Chu?n b? ki?n tr?c c? th? m? r?ng ti?p sang domain ri?ng, CI/CD v? autoscaling.

## Ki?n tr?c tri?n khai

```text
Ng??i d?ng
  -> Amazon CloudFront
  -> Amazon S3 (frontend React build)
  -> Application Load Balancer
  -> Amazon ECS Fargate (FastAPI backend)
  -> Amazon RDS for PostgreSQL
  -> Amazon S3 private bucket (CV v? file ??nh k?m)
  -> Amazon CloudWatch Logs / Alarms
```

## L? do ch?n d?ch v?

- [Amazon CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html): ph?n ph?i frontend nhanh, cache t?t v? h? tr? HTTPS.
- [Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html): l?u static frontend v? private resume storage chi ph? th?p.
- [Amazon ECS Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html): ch?y backend container m? kh?ng ph?i qu?n l? EC2.
- [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html): ph? h?p v?i d? li?u quan h? c?a user, profile, job, application v? master data.
- [Amazon CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html): thu log, theo d?i l?i v? c?nh b?o 5xx c? b?n.

## Lu?ng tri?n khai

1. Build frontend t? m? ngu?n React/Vite v? publish l?n S3.
2. C?u h?nh CloudFront ?? ph?n ph?i giao di?n v? tr? API v? ALB.
3. Build backend FastAPI th?nh Docker image, ??y l?n ECR v? ch?y b?ng ECS Fargate.
4. K?t n?i backend ??n RDS PostgreSQL v? bucket private ch?a CV.
5. Ki?m tra AI matching, upload CV, ?ng tuy?n v? duy?t tin theo lu?ng end-to-end.
