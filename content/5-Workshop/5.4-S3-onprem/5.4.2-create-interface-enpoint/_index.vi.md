---
title: "Đóng gói backend và triển khai lên ECS Fargate"
date: 2026-08-09
weight: 2
chapter: false
pre: " <b> 5.4.2. </b> "
---

## Bước 1: build image backend

```bash
cd backend
docker build -t jobgo-api:latest .
```

## Bước 2: đẩy image lên ECR

```bash
aws ecr get-login-password --region ap-southeast-1 | docker login --username AWS --password-stdin <account-id>.dkr.ecr.ap-southeast-1.amazonaws.com
docker tag jobgo-api:latest <account-id>.dkr.ecr.ap-southeast-1.amazonaws.com/jobgo-api:latest
docker push <account-id>.dkr.ecr.ap-southeast-1.amazonaws.com/jobgo-api:latest
```

## Bước 3: cấu hình task definition

Task definition cần khai báo:

- image từ ECR,
- cổng container `8000`,
- biến môi trường `DATABASE_URL`, `JWT_SECRET_KEY`, `AWS_REGION`, `S3_RESUME_BUCKET`,
- IAM task role cho quyền truy cập bucket CV và CloudWatch Logs.

## Bước 4: tạo ECS service

- Chọn launch type là [AWS Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html).
- Gắn service vào target group của ALB.
- Health check path nên là `/health`.
- Cấu hình desired count tối thiểu là `1` cho môi trường demo.
