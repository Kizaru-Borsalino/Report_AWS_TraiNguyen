---
title: "Deployment architecture overview"
date: 2026-08-05
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

## Context

JobGo is a recruitment platform for students and companies. The system supports:

- public job browsing for guests,
- candidate profile management, CV handling, applications, and application history,
- company profile management, job posting, and applicant review,
- administrator moderation, master data management, and platform supervision.

The distinctive capability is the **AI Matching Engine**: whenever a candidate updates the profile or a company opens the applicant list, the system recalculates the matching score based on skills, position, level, location, job type, and work mode.

## Technical Goals

- Separate frontend, backend, database, and file storage for clearer operations.
- Keep resumes private; every file request must pass through an authorized backend flow.
- Ensure the matching score can be recalculated when a candidate profile changes.
- Prepare the architecture for later expansion with a custom domain, CI/CD, and autoscaling.

## Deployment Architecture

```text
Users
  -> Amazon CloudFront
  -> Amazon S3 (React frontend build)
  -> Application Load Balancer
  -> Amazon ECS Fargate (FastAPI backend)
  -> Amazon RDS for PostgreSQL
  -> Amazon S3 private bucket (resumes and attachments)
  -> Amazon CloudWatch Logs / Alarms
```
![Architecture Diagram](/images/architecture_final.png)

## Why These Services

- [Amazon CloudFront](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html): fast frontend delivery, strong caching, and HTTPS support.
- [Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html): low-cost storage for static assets and private resumes.
- [Amazon ECS Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html): containerized backend deployment without managing EC2 servers.
- [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html): a good fit for relational entities such as users, profiles, jobs, applications, and master data.
- [Amazon CloudWatch](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html): centralized logs, basic failure monitoring, and alarms.

## Delivery Flow

1. Build the frontend from the React/Vite source and publish it to S3.
2. Configure CloudFront to serve the SPA and route API traffic to the ALB.
3. Build the FastAPI backend into a Docker image, push it to ECR, and run it on ECS Fargate.
4. Connect the backend to Amazon RDS for PostgreSQL and the private resume bucket.
5. Validate AI matching, resume upload, applications, and moderation through the end-to-end workflow.
