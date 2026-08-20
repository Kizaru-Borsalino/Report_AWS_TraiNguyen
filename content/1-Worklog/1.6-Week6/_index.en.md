---
title: "Week 6 - Role-based UI and reference data"
date: 2026-07-20
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Objectives

- Restructure the user interface into role-specific screens and task-focused pages.
- Synchronize master data across backend and frontend to avoid inconsistent free-text inputs.
- Publish the frontend production build on Amazon S3 and CloudFront.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Split the company dashboard into company profile, job creation, applicant list, and job list pages. | 20/07/2026 | 20/07/2026 | Company UX map |
| Tuesday | Split the student dashboard into profile, resumes, apply, and application history pages. | 21/07/2026 | 21/07/2026 | Student UX map |
| Wednesday | Built the admin master-data management APIs and screens. | 22/07/2026 | 22/07/2026 | Master data admin checklist |
| Thursday | Converted skills, locations, positions, and levels into normalized selection controls. | 23/07/2026 | 23/07/2026 | Reference data mapping |
| Friday | Built the frontend with Vite, published assets to S3, and configured CloudFront cache behavior. | 24/07/2026 | 24/07/2026 | S3 static hosting, CloudFront docs |
| Saturday | Verified that guests can browse public jobs while AI Matching remains hidden until registration. | 25/07/2026 | 25/07/2026 | Guest flow test plan |

### Outcomes

- The JobGo interface is now clearer by role and better suited for business-flow demonstrations.
- The frontend now has a production deployment path through S3 and CloudFront.
