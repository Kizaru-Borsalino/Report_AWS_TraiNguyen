---
title: "Week 3 - Candidate profiles and resume storage on S3"
date: 2026-06-29
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Objectives

- Complete candidate profiles and resume management using a secure file storage model.
- Integrate a private Amazon S3 bucket for resume upload and download.
- Ensure companies can only access resumes through authorized flows.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Designed the student profile with school, major, skills, desired position, and social links. | 29/06/2026 | 29/06/2026 | Profile field specification |
| Tuesday | Built the student profile update API and validated inputs against master data. | 30/06/2026 | 30/06/2026 | Profile API contract |
| Wednesday | Integrated resume uploads to a private S3 bucket and stored object keys in PostgreSQL. | 01/07/2026 | 01/07/2026 | Amazon S3 upload design |
| Thursday | Implemented presigned URLs to download resumes with proper authorization and expiration. | 02/07/2026 | 02/07/2026 | S3 presigned URL docs |
| Friday | Tested multi-resume upload, default resume selection, and deletion of unused resumes. | 03/07/2026 | 03/07/2026 | Resume management checklist |
| Saturday | Added file access and error logging for CloudWatch Logs monitoring. | 04/07/2026 | 04/07/2026 | CloudWatch logging notes |

### Outcomes

- Candidates can now manage their profiles and resumes using a production-ready AWS storage model.
- Resume access is more secure because files are never publicly exposed.
