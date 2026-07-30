---
title : "IAM, Security, and CORS"
date : 2024-01-01
weight : 5
chapter : false
pre : " <b> 5.5. </b> "
---

## IAM

The backend needs access to S3 to upload and read CV files. In production, attaching an IAM Role to EC2 is better than storing access keys in `.env`.

Applied principles:

- Grant only `s3:PutObject` and `s3:GetObject` on the CV bucket.
- Do not make the CV bucket public.
- Do not grant broad administrator permissions to the backend.

## Security Group

Security groups should be separated clearly:

- Backend EC2 receives requests from the frontend/API gateway or Nginx.
- RDS accepts connections only from the backend EC2.
- Port `8000` should only be opened temporarily for testing, then moved behind Nginx or an HTTPS endpoint.

## Production CORS

The backend should only allow the real frontend domain:

```env
BACKEND_CORS_ORIGINS=https://your-frontend-domain.com
BACKEND_CORS_ORIGIN_REGEX=
REFRESH_COOKIE_SECURE=true
REFRESH_COOKIE_SAMESITE=none
```

Wildcard CORS should not be used in production because it may increase the risk of API access from unwanted origins.

## CV Protection

CV files are protected by three layers:

1. Private S3 bucket.
2. Backend authorization check before creating a link.
3. Short-lived presigned URL, for example 300 seconds.
