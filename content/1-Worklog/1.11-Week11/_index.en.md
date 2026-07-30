---
title: "Week 11 - Frontend Deployment"
date: 2024-01-01
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Goals

- Build the React app for production.
- Deploy the frontend to S3 Static Website Hosting or CloudFront.
- Configure CORS between the frontend and backend.

### Work Completed

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| Day 1 | Configure `VITE_API_URL`<br>Frontend calls the production backend | 2025-10-20 | 2025-10-20 | Amazon S3 Hosting / CloudFront Docs |
| Day 2 | Build frontend<br>Created the Vite `dist` folder | 2025-10-21 | 2025-10-21 | Amazon S3 Hosting / CloudFront Docs |
| Day 3 | Upload to S3<br>Served static assets through S3/CloudFront | 2025-10-22 | 2025-10-22 | Amazon S3 Hosting / CloudFront Docs |
| Day 4 | Configure backend CORS<br>Allowed only the valid frontend domain | 2025-10-23 | 2025-10-23 | Amazon S3 Hosting / CloudFront Docs |

### Results

The frontend can be accessed from a browser through AWS hosting. The application connects to the production backend and is ready for an end-to-end demo.
