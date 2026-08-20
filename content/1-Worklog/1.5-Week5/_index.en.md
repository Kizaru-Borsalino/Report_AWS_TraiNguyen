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
| Monday | Built the application API with resume selection, cover letter support, and duplicate checks. | 13/07/2026 | 13/07/2026 | Application API contract |
| Tuesday | Implemented application status history plus withdraw-and-reapply capability. | 14/07/2026 | 14/07/2026 | Application status model |
| Wednesday | Implemented the admin approval flow before jobs become public. | 15/07/2026 | 15/07/2026 | Admin moderation checklist |
| Thursday | Generated notifications for new applications, status updates, and approved job posts. | 16/07/2026 | 16/07/2026 | Notification flow design |
| Friday | Created the task definition, service, and ALB target group for the staging backend on ECS Fargate. | 17/07/2026 | 17/07/2026 | ECS Fargate deployment notes |
| Saturday | Executed end-to-end smoke tests against the staging environment using seed data. | 18/07/2026 | 18/07/2026 | Staging smoke test checklist |

### Outcomes

- The core application lifecycle is complete and demonstrable on AWS staging.
- Administrators can now control job quality before listings are made public.
