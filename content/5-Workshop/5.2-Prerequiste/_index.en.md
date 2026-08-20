---
title: "Prerequisites"
date: 2026-08-05
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

## Accounts and Tools

- An AWS account with access to [Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html), [Amazon CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html), [Amazon ECR](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html), [Amazon ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html), [Amazon RDS](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html), [IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html), and [CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html).
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html) configured with a profile.
- [Docker](https://docs.docker.com/get-started/get-docker/), [Node.js](https://nodejs.org/en/download), [npm](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm), and [Python](https://www.python.org/downloads/).
- Working familiarity with [FastAPI](https://fastapi.tiangolo.com/), [React](https://react.dev/learn), and [Vite](https://vite.dev/guide/).

## Source Layout

```text
frontend/
  src/
  public/
backend/
  app/
  requirements.txt
  Dockerfile
```

## Minimum Production Variables

Backend:

```env
DATABASE_URL=postgresql://jobgo_user:***@jobgo-db.abcdef.ap-southeast-1.rds.amazonaws.com:5432/jobgo
JWT_SECRET_KEY=change-me
AWS_REGION=ap-southeast-1
S3_RESUME_BUCKET=jobgo-resume-prod
CORS_ORIGINS=https://jobgo.example.com
```

Frontend:

```env
VITE_API_BASE_URL=https://api.jobgo.example.com
```

## Required Seed Data

- Master data for `skills`, `positions`, `levels`, `locations`, `job types`, and `work modes`.
- At least 1 candidate account, 1 company account, and 1 administrator account.
- At least 1 candidate profile and 1 job posting to validate AI matching.
