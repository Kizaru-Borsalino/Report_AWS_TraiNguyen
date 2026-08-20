---
title: "?i?u ki?n chu?n b?"
date: 2026-08-05
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

## T?i kho?n v? c?ng c?

- T?i kho?n AWS c? quy?n v?i [Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html), [Amazon CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html), [Amazon ECR](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html), [Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html), [Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html), [IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html) v? [CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html).
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) ?? c?u h?nh profile.
- [Docker](https://docs.docker.com/get-started/get-docker/), [Node.js](https://nodejs.org/en/download), [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) v? [Python](https://www.python.org/downloads/).
- Ki?n th?c c? b?n v? [FastAPI](https://fastapi.tiangolo.com/), [React](https://react.dev/learn) v? [Vite](https://vite.dev/guide/).

## C?u tr?c m? ngu?n

```text
frontend/
  src/
  public/
backend/
  app/
  requirements.txt
  Dockerfile
```

## Bi?n m?i tr??ng production

Backend c?n t?i thi?u:

```env
DATABASE_URL=postgresql://jobgo_user:***@jobgo-db.abcdef.ap-southeast-1.rds.amazonaws.com:5432/jobgo
JWT_SECRET_KEY=change-me
AWS_REGION=ap-southeast-1
S3_RESUME_BUCKET=jobgo-resume-prod
CORS_ORIGINS=https://jobgo.example.com
```

Frontend c?n t?i thi?u:

```env
VITE_API_BASE_URL=https://api.jobgo.example.com
```

## D? li?u ph?i c? tr??c khi test

- Master data cho `k? n?ng`, `v? tr?`, `c?p b?c`, `??a ?i?m`, `lo?i h?nh`, `h?nh th?c l?m vi?c`.
- ?t nh?t 1 t?i kho?n ?ng vi?n, 1 t?i kho?n doanh nghi?p v? 1 t?i kho?n qu?n tr? vi?n.
- ?t nh?t 1 h? s? ?ng vi?n v? 1 tin tuy?n d?ng ?? ki?m th? AI Matching.
