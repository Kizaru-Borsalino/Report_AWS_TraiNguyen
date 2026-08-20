---
title: "Security, IAM, logging, and validation"
date: 2026-08-11
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

## IAM and least privilege

- The ECS task role only needs `s3:GetObject` and `s3:PutObject` on the resume bucket.
- Only the release identity should be able to push images to ECR and update the ECS service.
- Do not hard-code access keys in the source code; store secrets in [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) or [AWS Secrets Manager](https://docs.aws.amazon.com/secretsmanager/latest/userguide/intro.html).

## Network security

- Only the ALB is public; ECS and RDS stay in private subnets.
- The RDS security group only opens PostgreSQL to the ECS security group.
- The resume bucket remains fully private; the frontend never reads it directly.

## CORS and file upload validation

- `CORS_ORIGINS` should only allow the JobGo frontend domain.
- The backend validates file type, file size, and access rights before exposing or downloading a CV.

## Logging and alarms

- Send application logs to CloudWatch Logs per ECS task.
- Create alarms for ALB 5xx errors, abnormal ECS CPU/Memory, and RDS connectivity issues.
- Track key audit events: login, job creation, application submission, and application status updates.
