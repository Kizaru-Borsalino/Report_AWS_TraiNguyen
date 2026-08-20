---
title: "Validate APIs, resume upload, and observability"
date: 2026-08-10
weight: 3
chapter: false
pre: " <b> 5.4.3. </b> "
---

## Backend validation

```bash
curl https://api.jobgo.example.com/health
curl https://api.jobgo.example.com/api/jobs
```

## Core business validation

1. A candidate registers and creates the profile.
2. The candidate uploads a resume through the backend into the private bucket.
3. A company creates a job posting with skills, position, level, and location.
4. The jobs page shows the **AI Matching** percentage once the candidate profile exists.
5. When the candidate clicks apply, the system creates the `application`, stores the cover letter, and reflects it in the application history.
6. The company opens the applicant list to review the matching score, cover letter, submitted CV, and application status.

## Observability

- Inspect backend logs in [CloudWatch Logs](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/WhatIsCloudWatchLogs.html).
- Track 4xx/5xx errors on the ALB and ECS service.
- Validate the log trail for resume uploads, job creation, application submission, and application status updates.
