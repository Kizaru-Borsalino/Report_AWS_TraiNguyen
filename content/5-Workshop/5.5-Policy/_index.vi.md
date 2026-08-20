---
title: "B?o m?t, IAM, logging v? validation"
date: 2026-08-11
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

## IAM v? nguy?n t?c quy?n h?n t?i thi?u

- ECS task role ch? ???c quy?n `s3:GetObject`, `s3:PutObject` tr?n bucket CV.
- T?i kho?n build/release m?i c? quy?n push image l?n ECR v? c?p nh?t ECS service.
- Kh?ng hard-code access key trong source; b? m?t n?n ??t trong [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) ho?c [AWS Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html).

## B?o m?t t?ng m?ng

- Ch? ALB public; ECS v? RDS ??t trong private subnet.
- Security group c?a RDS ch? m? c?ng PostgreSQL cho security group c?a ECS.
- Bucket CV gi? private ho?n to?n; frontend kh?ng truy c?p tr?c ti?p.

## CORS v? upload file

- `CORS_ORIGINS` ch? cho ph?p domain frontend c?a JobGo.
- Backend ki?m tra lo?i file, k?ch th??c file v? quy?n truy c?p tr??c khi cho t?i ho?c xem CV.

## Logging v? c?nh b?o

- G?i log ?ng d?ng v?o CloudWatch Logs theo t?ng ECS task.
- T?o alarm cho 5xx ? ALB, CPU/Memory b?t th??ng ? ECS v? t?nh tr?ng k?t n?i RDS.
- Ghi l?i c?c event quan tr?ng: ??ng nh?p, t?o tin, ?ng tuy?n, thay ??i tr?ng th?i ?ng tuy?n.
