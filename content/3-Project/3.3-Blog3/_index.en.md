---
title: "Business Flow and Testing"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

## Main Demo Flow

1. A company registers or logs in.
2. The company creates a company profile.
3. The company publishes an internship position.
4. An admin logs in and approves the post.
5. A student registers or logs in.
6. The student creates a profile and uploads a CV.
7. The student views approved internship posts and applies.
8. The company views the applicant list.
9. The company opens the CV through a presigned URL.
10. The company updates the application status.
11. The student receives a status notification.

## Test Cases

The backend includes automated tests for important flows:

- Company creates an internship post.
- Admin approves the post.
- Student uploads CV and applies.
- Company updates application status.
- Notification is created when status changes.
- Duplicate applications are blocked.
- Expired deadlines are blocked.
- Locked accounts are blocked.
- Admin/company/student authorization is checked.
- GPA, recruitment quantity, and CV file size are validated.
- Analytics for skills, positions, salary, and locations are tested.
- Forum features are tested: posting, approval, comments, likes, saves, and moderation.

## Result

After development and testing, the project supports the main business flow of an internship management system. It can run locally with SQLite for quick demos and has production configuration for AWS deployment with RDS PostgreSQL, S3, EC2, and CloudWatch.
