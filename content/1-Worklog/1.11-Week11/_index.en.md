---
title: "Week 11 - AWS deployment hardening and operations"
date: 2026-08-24
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Objectives

- Finalize the AWS production setup for frontend, backend, database, and storage.
- Improve observability, configuration security, and basic backup readiness.
- Prepare the build pipeline and deployment checklist.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Reviewed the ECS service, autoscaling policy, health checks, and rollback strategy for the JobGo backend. | 24/08/2026 | 24/08/2026 | ECS operations checklist |
| Tuesday | Standardized secrets management using Systems Manager Parameter Store or AWS Secrets Manager. | 25/08/2026 | 25/08/2026 | Secrets management notes |
| Wednesday | Configured CloudWatch Logs, metric filters, and alarms for critical backend failures. | 26/08/2026 | 26/08/2026 | CloudWatch alarms guide |
| Thursday | Reviewed the RDS snapshot policy and S3 versioning for the resume bucket. | 27/08/2026 | 27/08/2026 | RDS backup, S3 versioning docs |
| Friday | Completed the deployment checklist: build frontend, push the ECR image, update the ECS service, and invalidate CloudFront cache. | 28/08/2026 | 28/08/2026 | Deployment runbook |
| Saturday | Ran a production-like smoke test and confirmed that guest, student, company, and admin flows all work correctly. | 29/08/2026 | 29/08/2026 | Production smoke test checklist |

### Outcomes

- The AWS deployment architecture is ready for the final demonstration with stronger operational realism.
- Infrastructure components now have clearer monitoring and change-control procedures.
