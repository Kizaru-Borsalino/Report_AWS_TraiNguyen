---
title: "Prerequisites"
date: 2026-08-05
weight: 2
chapter: false
pre: " <b> 5.2. </b> "
---

## Requirements

- An AWS account with access to S3, CloudFront, ECS, ECR, RDS, IAM, and CloudWatch
- Docker to build the backend image
- Node.js to build the frontend
- AWS CLI for optional operational steps
- Production environment variables for the backend
- Seed data for accounts, master data, and roles

## Expected output

After finishing the workshop, the reader should be able to:

- open the JobGo frontend through CloudFront,
- call the backend API through the ALB,
- verify that the backend can reach RDS,
- upload resumes into the private S3 bucket,
- inspect backend logs in CloudWatch.
