---
title: "??ng g?i backend v? tri?n khai l?n ECS Fargate"
date: 2026-08-09
weight: 2
chapter: false
pre: " <b> 5.4.2. </b> "
---

## B??c 1: build image backend

```bash
cd backend
docker build -t jobgo-api:latest .
```

## B??c 2: ??y image l?n ECR

```bash
aws ecr get-login-password --region ap-southeast-1 | docker login --username AWS --password-stdin <account-id>.dkr.ecr.ap-southeast-1.amazonaws.com
docker tag jobgo-api:latest <account-id>.dkr.ecr.ap-southeast-1.amazonaws.com/jobgo-api:latest
docker push <account-id>.dkr.ecr.ap-southeast-1.amazonaws.com/jobgo-api:latest
```

## B??c 3: c?u h?nh task definition

Task definition c?n khai b?o:

- image t? ECR,
- c?ng container `8000`,
- bi?n m?i tr??ng `DATABASE_URL`, `JWT_SECRET_KEY`, `AWS_REGION`, `S3_RESUME_BUCKET`,
- IAM task role cho quy?n truy c?p bucket CV v? CloudWatch Logs.

## B??c 4: t?o ECS service

- Ch?n launch type l? [AWS Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html).
- G?n service v?o target group c?a ALB.
- Health check path n?n l? `/health`.
- C?u h?nh desired count t?i thi?u l? `1` cho m?i tr??ng demo.
