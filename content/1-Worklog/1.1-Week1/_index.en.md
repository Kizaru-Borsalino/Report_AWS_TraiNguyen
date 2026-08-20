---
title: "Week 1 - Project kickoff and requirement analysis"
date: 2026-06-15
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Objectives

- Understand the recruitment portal problem space for guests, candidates, companies, and administrators.
- Break the problem down into use cases, user flows, and an MVP scope before drafting the detailed SRS.
- Establish an AWS-oriented target design early so the project is not treated as a local-only prototype.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Analyzed the recruitment platform needs, including public job discovery, registration, profile management, application flow, job moderation, and shared data management. | 15/06/2026 | 15/06/2026 | [AWS Well-Architected Framework](https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html) |
| Tuesday | Identified actors, use cases, and role-specific pain points to define clear boundaries for guest, candidate, company, and admin workflows. | 16/06/2026 | 16/06/2026 | [AWS Prescriptive Guidance - Microservice decomposition](https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-decomposing-monoliths/welcome.html) |
| Wednesday | Locked the initial MVP scope: authentication, candidate profile, company profile, job posting, applications, approval workflow, and first-phase AI matching. | 17/06/2026 | 17/06/2026 | [Amazon Cognito features](https://docs.aws.amazon.com/cognito/latest/developerguide/features.html) |
| Thursday | Drafted the first SRS structure and defined the core business fields, validations, and status lifecycles. | 18/06/2026 | 18/06/2026 | [IBM - Software requirements specification](https://www.ibm.com/think/topics/software-requirements-specification) |
| Friday | Drafted the target AWS architecture with CloudFront, S3, ALB, ECS Fargate, RDS PostgreSQL, a private S3 bucket for resumes, and CloudWatch for logging. | 19/06/2026 | 19/06/2026 | [AWS Architecture Center](https://aws.amazon.com/architecture/), [AWS Architecture Icons](https://aws.amazon.com/architecture/icons/) |
| Saturday | Converted the analysis into a technical backlog covering frontend, backend, master data, CV storage, matching engine, and admin workflows. | 20/06/2026 | 20/06/2026 | [FastAPI documentation](https://fastapi.tiangolo.com/), [Vite Guide](https://vite.dev/guide/) |

### Outcomes

- The first week now reflects a proper **project kickoff flow**: requirement discovery, actors, use cases, and business scope first, followed by the SRS direction.
- The team entered the next phase with a clear foundation for SRS completion, data design, API planning, and AWS deployment preparation.
