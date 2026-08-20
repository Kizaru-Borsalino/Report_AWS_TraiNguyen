---
title: "D?n d?p t?i nguy?n v? b?n giao"
date: 2026-08-12
weight: 6
chapter: false
pre: " <b> 5.6. </b> "
---

## D?n d?p t?i nguy?n

1. X?a CloudFront distribution sau khi ?? disable.
2. X?a n?i dung bucket frontend v? bucket CV n?u kh?ng c?n l?u gi?.
3. Scale ECS service v? `0` ho?c x?a service, task definition kh?ng c?n d?ng.
4. X?a image c? trong ECR.
5. Snapshot RDS tr??c khi x?a database.
6. X?a alarm v? log group kh?ng c?n s? d?ng ?? tr?nh ph?t sinh chi ph?.

## G?i b?n giao

- S? ?? ki?n tr?c JobGo tr?n AWS.
- Danh s?ch bi?n m?i tr??ng production.
- Checklist build frontend, push image, update ECS service v? invalidation CloudFront.
- Danh s?ch master data ph?c v? AI Matching.
- T?i li?u ki?m th? lu?ng guest, ?ng vi?n, doanh nghi?p v? admin.

## H??ng ph?t tri?n ti?p theo

- T?ch h?p CI/CD b?ng GitHub Actions v? AWS CodeDeploy ho?c ECS deployment workflow.
- G?n domain ri?ng v?i [AWS Certificate Manager](https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html) v? [Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html).
- N?ng c?p AI Matching t? rule-based sang m? h?nh semantic ho?c embedding khi c? d? li?u ?? l?n.
