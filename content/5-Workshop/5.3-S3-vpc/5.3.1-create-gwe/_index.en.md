---
title : "Create Private CV Bucket"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.3.1. </b> "
---

## Steps

1. Open the Amazon S3 Console.
2. Choose **Create bucket**.
3. Select region `ap-southeast-1`.
4. Name the bucket for the project, for example `internship-portal-cv-bucket`.
5. Enable **Block all public access**.
6. Enable encryption using SSE-S3 or SSE-KMS.
7. Create the bucket.

## Why Private Configuration Is Required

CV files contain student personal data, so they must not be exposed publicly. The backend controls access and only generates temporary presigned URLs for authorized users.

## Result

The S3 bucket is ready for the backend to upload CV files and manage them by object key.
