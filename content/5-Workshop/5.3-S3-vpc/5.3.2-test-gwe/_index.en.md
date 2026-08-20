---
title: "Configure CloudFront and validate the frontend"
date: 2026-08-07
weight: 2
chapter: false
pre: " <b> 5.3.2. </b> "
---

## Core Configuration

- Create a distribution with `jobgo-frontend-prod` as the origin.
- Enable [Origin Access Control](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) so the bucket stays private.
- Set `index.html` as the default root object.
- Configure custom error responses `403/404 -> /index.html` for SPA routing.

## Cache invalidation after release

```bash
aws cloudfront create-invalidation \
  --distribution-id E1234567890 \
  --paths "/*"
```

## Validation Checklist

- The home page shows public job listings for guests.
- The `Login` button opens the authentication form instead of blocking anonymous users.
- The frontend targets the production API through `VITE_API_BASE_URL`.
- The job detail route still works when the page is refreshed.
