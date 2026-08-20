---
title: "Week 11 - AWS deployment plan and release validation"
date: 2026-08-24
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Objectives

- Prepare JobGo for release on an AWS production-like architecture.
- Finalize the build, release, smoke test, and basic observability flow.
- Verify that the primary business journeys remain stable after cloud-oriented configuration.

### Planned Tasks

| Day | Planned task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Create the ECR repository, build the FastAPI backend image, and prepare the ECS Fargate task definition. | 24/08/2026 | 24/08/2026 | [Amazon ECR User Guide](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html), [Amazon ECS Developer Guide](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html) |
| Tuesday | Provision Amazon RDS for PostgreSQL, security groups, a subnet group, and production environment variables for the backend. | 25/08/2026 | 25/08/2026 | [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html) |
| Wednesday | Build the Vite frontend, upload static assets to S3, and distribute them through CloudFront using Origin Access Control. | 26/08/2026 | 26/08/2026 | [Hosting a static website on Amazon S3](https://docs.aws.amazon.com/AmazonS3/latest/userguide/WebsiteHosting.html), [CloudFront Developer Guide](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html) |
| Thursday | Configure the private resume bucket, CORS, the ECS task IAM role, and file access permissions. | 27/08/2026 | 27/08/2026 | [Amazon S3 security best practices](https://docs.aws.amazon.com/AmazonS3/latest/userguide/security-best-practices.html), [IAM best practices](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html) |
| Friday | Configure CloudWatch Logs, the `/health` check, 5xx alarms, and smoke tests for guest, candidate, company, and admin flows. | 28/08/2026 | 28/08/2026 | [Using Amazon CloudWatch alarms](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/AlarmThatSendsEmail.html) |
| Saturday | Run the end-to-end validation flow: public job browsing, profile updates, AI matching, applications, moderation, and application status tracking. | 29/08/2026 | 29/08/2026 | [Application Load Balancer health checks](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/target-group-health-checks.html) |

### Expected Outcome

- By the end of week 11, JobGo is presented as a deployment-ready AWS solution with frontend, backend, database, private file storage, and monitoring.
- This entry is written as a **planned deployment worklog** for `24/08/2026 - 29/08/2026`, because those dates are still ahead of the current day.
