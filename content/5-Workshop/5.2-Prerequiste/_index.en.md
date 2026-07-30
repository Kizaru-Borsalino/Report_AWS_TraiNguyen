---
title : "Preparing AWS Environment"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.2. </b> "
---

## 1. Select Region

The recommended deployment region is:

```text
ap-southeast-1
```

Using one region reduces complexity when configuring EC2, RDS, S3, IAM, and CloudWatch.

## 2. Prepare IAM

An IAM user or role should have permission to work with:

- EC2
- RDS
- S3
- IAM
- CloudWatch

For production deployment, attaching an **IAM Role** to EC2 is preferred over storing access keys directly in `.env`.

## 3. Prepare Backend Environment

Main backend variables:

```env
DATABASE_URL=postgresql+psycopg2://app_user:<password>@<rds-endpoint>:5432/internship_portal
AWS_REGION=ap-southeast-1
S3_BUCKET_NAME=<your-cv-bucket>
S3_PRESIGNED_URL_EXPIRE_SECONDS=300
BACKEND_CORS_ORIGINS=https://your-frontend-domain.com
REFRESH_COOKIE_SECURE=true
REFRESH_COOKIE_SAMESITE=none
```

## 4. Prepare Frontend Environment

The frontend must point to the production API:

```env
VITE_API_URL=https://your-api-domain.com
```

Then build the frontend:

```powershell
cd frontend
npm.cmd install
npm.cmd run build
```
