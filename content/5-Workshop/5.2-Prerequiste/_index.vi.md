---
title: "Điều kiện chuẩn bị"
date: 2026-08-05
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

## Tài khoản và công cụ

- Tài khoản AWS có quyền với [Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html), [Amazon CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html), [Amazon ECR](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html), [Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html), [Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html), [IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html) và [CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html).
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) đã cấu hình profile.
- [Docker](https://docs.docker.com/get-started/get-docker/), [Node.js](https://nodejs.org/en/download), [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm) và [Python](https://www.python.org/downloads/).
- Kiến thức cơ bản về [FastAPI](https://fastapi.tiangolo.com/), [React](https://react.dev/learn) và [Vite](https://vite.dev/guide/).

## Cấu trúc mã nguồn

```text
frontend/
  src/
  public/
backend/
  app/
  requirements.txt
  Dockerfile
```

## Biến môi trường production

Backend cần tối thiểu:

```env
DATABASE_URL=postgresql://jobgo_user:***@jobgo-db.abcdef.ap-southeast-1.rds.amazonaws.com:5432/jobgo
JWT_SECRET_KEY=change-me
AWS_REGION=ap-southeast-1
S3_RESUME_BUCKET=jobgo-resume-prod
CORS_ORIGINS=https://jobgo.example.com
```

Frontend cần tối thiểu:

```env
VITE_API_BASE_URL=https://api.jobgo.example.com
```

## Dữ liệu phải có trước khi test

- Master data cho `kỹ năng`, `vị trí`, `cấp bậc`, `địa điểm`, `loại hình`, `hình thức làm việc`.
- Ít nhất 1 tài khoản ứng viên, 1 tài khoản doanh nghiệp và 1 tài khoản quản trị viên.
- Ít nhất 1 hồ sơ ứng viên và 1 tin tuyển dụng để kiểm thử AI Matching.
