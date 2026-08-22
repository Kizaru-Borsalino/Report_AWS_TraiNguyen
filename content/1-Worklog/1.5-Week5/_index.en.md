---
title: "Week 5 - Applications, status management, and approval flow"
date: 2026-07-13
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Objectives

- Connect the complete application lifecycle across candidates, companies, and admins.
- Manage application statuses and notifications.
- Run the backend on Amazon ECS Fargate in the staging environment.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Built the application API with resume selection, cover letter support, and duplicate checks. | 13/07/2026 | 13/07/2026 | [OpenAPI Specification](https://swagger.io/specification/), [REST API Design Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design) |
| Tuesday | Implemented application status history plus withdraw-and-reapply capability. | 14/07/2026 | 14/07/2026 | [State Machine Design Pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/state-machine) |
| Wednesday | Implemented the admin approval flow before jobs become public. | 15/07/2026 | 15/07/2026 | [OWASP Authorization Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authorization_Cheat_Sheet.html) |
| Thursday | Generated notifications for new applications, status updates, and approved job posts. | 16/07/2026 | 16/07/2026 | [Amazon EventBridge User Guide](https://docs.aws.amazon.com/eventbridge/latest/userguide/eb-what-is.html), [Designing notifications](https://www.nngroup.com/articles/notification-design/) |
| Friday | Created the task definition, service, and ALB target group for the staging backend on ECS Fargate. | 17/07/2026 | 17/07/2026 | [Amazon ECS on AWS Fargate](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/AWS_Fargate.html) |
| Saturday | Executed end-to-end smoke tests against the staging environment using seed data. | 18/07/2026 | 18/07/2026 | [Playwright Docs](https://playwright.dev/docs/intro), [AWS Well-Architected Operational Excellence](https://docs.aws.amazon.com/wellarchitected/latest/operational-excellence-pillar/welcome.html) |

### Outcomes

- The core application lifecycle is complete and demonstrable on AWS staging.
- Administrators can now control job quality before listings are made public.


