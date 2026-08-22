---
title: "Week 4 - Company profiles and job posting flow"
date: 2026-07-06
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Objectives

- Deliver company-facing features: company profile, job creation, and job listing management.
- Normalize shared master data used by both jobs and profiles.
- Prepare the backend container for ECS deployment.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Designed the company profile including company name, website, size, industry, address, and benefits. | 06/07/2026 | 06/07/2026 | [Schema.org Organization](https://schema.org/Organization) |
| Tuesday | Built APIs to create and update job posts with position, skills, salary range, work mode, and level. | 07/07/2026 | 07/07/2026 | [REST API Design Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design), [Pydantic Models](https://docs.pydantic.dev/latest/concepts/models/) |
| Wednesday | Completed the company job list with draft, pending approval, and published statuses. | 08/07/2026 | 08/07/2026 | [State Machine Design Pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/state-machine) |
| Thursday | Created master data tables for skills, positions, locations, employment type, work mode, and level. | 09/07/2026 | 09/07/2026 | [PostgreSQL Documentation](https://www.postgresql.org/docs/current/index.html), [Database normalization](https://www.ibm.com/think/topics/database-normalization) |
| Friday | Containerized the backend with Docker and prepared the image for Amazon ECR. | 10/07/2026 | 10/07/2026 | [Dockerfile reference](https://docs.docker.com/reference/dockerfile/), [Amazon ECR User Guide](https://docs.aws.amazon.com/AmazonECR/latest/userguide/what-is-ecr.html) |
| Saturday | Tested company profile and role-based job posting flows. | 11/07/2026 | 11/07/2026 | [Playwright Docs](https://playwright.dev/docs/intro), [Testing Library Guiding Principles](https://testing-library.com/docs/guiding-principles/) |

### Outcomes

- Companies can now manage their information and create job posts with normalized data.
- The backend is ready for container-based deployment on AWS.


