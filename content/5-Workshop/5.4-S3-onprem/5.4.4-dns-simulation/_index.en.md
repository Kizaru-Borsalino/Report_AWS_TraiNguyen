---
title : "Deploy Frontend"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4.4. </b> "
---

## Configure API URL

In `frontend/.env`, configure:

```env
VITE_API_URL=https://your-api-domain.com
```

If testing directly with the EC2 public IP:

```env
VITE_API_URL=http://<ec2-public-ip>:8000
```

## Build Frontend

```powershell
cd frontend
npm.cmd install
npm.cmd run build
```

The build output is in the `dist` folder.

## Upload to S3

```powershell
aws s3 sync dist/ s3://<your-frontend-bucket> --delete
```

## Configure Hosting

Two options:

- **S3 Static Website Hosting:** suitable for quick demos.
- **CloudFront + S3:** better for production because it supports HTTPS, caching, and content distribution.

## Test

Open the frontend domain, log in with demo accounts, and check whether the student, company, and admin pages can call the backend API.
