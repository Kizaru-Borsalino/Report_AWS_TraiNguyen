---
title: "Week 1 - Requirements discovery and JobGo architecture"
date: 2026-06-15
weight: 1
chapter: false
pre: " <b> 1.1. </b> "
---

### Objectives

- Understand the business scope of the JobGo recruitment portal for students, companies, and administrators.
- Translate the SRS into a technical backlog and an AWS deployment architecture.
- Establish development standards, repository structure, and API conventions.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Reviewed the SRS, use cases, and actor list to define the MVP scope of JobGo. | 15/06/2026 | 15/06/2026 | JobGo SRS, use case backlog |
| Tuesday | Drafted the target AWS architecture using CloudFront, S3, ECS Fargate, ALB, RDS PostgreSQL, and a private S3 bucket for resumes. | 16/06/2026 | 16/06/2026 | AWS Architecture Icons, ECS/RDS/S3 docs |
| Wednesday | Created the first sprint backlog covering authentication, profiles, job posting, and admin approval. | 17/06/2026 | 17/06/2026 | Sprint planning board |
| Thursday | Bootstrapped the monorepo structure for the React frontend and FastAPI backend. | 18/06/2026 | 18/06/2026 | Frontend/Backend project template |
| Friday | Designed the initial data model for users, profiles, jobs, applications, resumes, and master data. | 19/06/2026 | 19/06/2026 | ERD draft, PostgreSQL notes |
| Saturday | Aligned API naming, role-based access rules, and acceptance criteria for the next sprint. | 20/06/2026 | 20/06/2026 | API conventions, acceptance checklist |

### Outcomes

- Completed the high-level JobGo architecture on AWS and identified the core production services.
- Prepared the team to move into authentication, data modeling, and foundational API implementation.
