---
title: "Week 6 - Develop a detailed statistics page and test the entire interface."
date: 2024-01-01
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Goals

- Design a secure way to store CV files.
- Integrate the backend with Amazon S3.
- Ensure that only authorized users can view CVs.

### Work Completed

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| 2 | Build the Career Market Insights page to display statistics on skills, roles, locations, and prevailing salary ranges.<br> | 13/07/2026 | 15/07/2026 | Analytics / API Docs |
| 5 | Test the interface across different user roles; handle UI bugs; verify loading states, empty states, and API error notifications.<br> | 16/07/2026 | 18/07/2026 | React Testing / Checklist |

### Results

CV files are handled more securely: files are stored in a private S3 bucket, backend controls access, and only authorized users receive short-lived presigned URLs.
