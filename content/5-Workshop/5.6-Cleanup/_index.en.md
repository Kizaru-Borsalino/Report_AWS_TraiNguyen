---
title: "Cleanup and handover"
date: 2026-08-12
weight: 6
chapter: false
pre: " <b> 5.6. </b> "
---

## Resource cleanup

1. Disable and remove the CloudFront distribution.
2. Empty and delete the frontend bucket and resume bucket if retention is not required.
3. Scale the ECS service to `0` or delete the service and unused task definitions.
4. Remove obsolete ECR images.
5. Create a final RDS snapshot before deleting the database.
6. Delete alarms and unused log groups to prevent unnecessary charges.

## Handover package

- The JobGo architecture diagram on AWS.
- The production environment variable inventory.
- The release checklist for frontend build, image push, ECS service update, and CloudFront invalidation.
- The master data inventory used by AI Matching.
- The test script for guest, candidate, company, and admin journeys.

## Future improvements

- Add CI/CD with GitHub Actions and AWS CodeDeploy or an ECS deployment workflow.
- Attach a custom domain using [AWS Certificate Manager](https://docs.aws.amazon.com/acm/latest/userguide/acm-overview.html) and [Amazon Route 53](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/Welcome.html).
- Upgrade the AI Matching engine from rule-based scoring to semantic or embedding-based matching once enough data is available.
