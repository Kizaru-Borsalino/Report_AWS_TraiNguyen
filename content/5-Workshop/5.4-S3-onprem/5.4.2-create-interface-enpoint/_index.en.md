---
title: "Containerize the backend and deploy to ECS Fargate"
date: 2026-08-09
weight: 2
chapter: false
pre: " <b> 5.4.2. </b> "
---

## Step 1: build the backend image

```bash
cd backend
docker build -t jobgo-api:latest .
```

## Step 2: push the image to ECR

```bash
aws ecr get-login-password --region ap-southeast-1 | docker login --username AWS --password-stdin <account-id>.dkr.ecr.ap-southeast-1.amazonaws.com
docker tag jobgo-api:latest <account-id>.dkr.ecr.ap-southeast-1.amazonaws.com/jobgo-api:latest
docker push <account-id>.dkr.ecr.ap-southeast-1.amazonaws.com/jobgo-api:latest
```

## Step 3: configure the task definition

The task definition should include:

- the ECR image,
- container port `8000`,
- environment variables such as `DATABASE_URL`, `JWT_SECRET_KEY`, `AWS_REGION`, and `S3_RESUME_BUCKET`,
- an IAM task role with access to the resume bucket and CloudWatch Logs.

## Step 4: create the ECS service

- Use [AWS Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html) as the launch type.
- Attach the service to the ALB target group.
- Set `/health` as the health check path.
- Keep the desired count at `1` for the demo environment.
