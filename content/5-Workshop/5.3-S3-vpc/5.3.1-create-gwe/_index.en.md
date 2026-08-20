---
title: "Build the frontend and upload to S3"
date: 2026-08-06
weight: 1
chapter: false
pre: " <b> 5.3.1. </b> "
---

## Step 1: configure the build variable

```env
VITE_API_BASE_URL=https://api.jobgo.example.com
```

## Step 2: build the frontend

```bash
cd frontend
npm ci
npm run build
```

This produces the `dist/` folder containing the HTML, CSS, JavaScript, and static assets.

## Step 3: create the frontend bucket

```bash
aws s3 mb s3://jobgo-frontend-prod --region ap-southeast-1
aws s3 sync dist s3://jobgo-frontend-prod --delete
```

## Step 4: deployment notes

- If [Origin Access Control](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) is used, the bucket does not need to be public.
- For a React SPA, CloudFront should return `index.html` for client-side routes that do not map to physical files.
- Each new release only needs a fresh build and another sync into the bucket.
