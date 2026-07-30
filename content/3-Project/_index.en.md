---
title: "Project"
date: 2024-01-01
weight: 3
chapter: false
pre: " <b> 3. </b> "
---

This section describes the practical project built by the team to apply backend, frontend, and AWS knowledge to a real-world student internship management problem.

### Main Sections

1. [Backend API](3.1-Blog1/)
2. [Frontend Application](3.2-Blog2/)
3. [Business Flow and Testing](3.3-Blog3/)
4. [Blogs Posted](3.4-BlogsPosted/)

## Technology Stack

| Component | Technology |
| --- | --- |
| Frontend | ReactJS, Vite, lucide-react |
| Backend | FastAPI, SQLAlchemy, Pydantic |
| Authentication | JWT, refresh token |
| Local database | SQLite |
| Production database | Amazon RDS PostgreSQL |
| File storage | Amazon S3 |
| Deployment | EC2, S3 Static Website Hosting/CloudFront |
| Monitoring | CloudWatch Logs |

## Key Features

### Student

- Register and log in.
- Create and update a personal profile.
- Upload CV.
- View and search internship positions.
- Search companies by name, description, or location.
- Submit applications.
- Track application status and receive notifications when the status changes.
- View market insights such as popular skills, positions, salary ranges, and recruitment locations.

### Company

- Register and log in.
- Create a company profile.
- Publish internship posts.
- View applicant lists.
- View applicant CVs through presigned URLs.
- Update application statuses: `Pending`, `Reviewed`, `Interview`, `Accepted`, `Rejected`.
- Receive notifications when an admin approves or rejects a post.

### Admin

- Manage user accounts.
- Lock or unlock accounts.
- Approve, reject, close, or delete internship posts.
- Manage skill and job-position lists.
- Moderate the community forum.
- View an overview dashboard.
