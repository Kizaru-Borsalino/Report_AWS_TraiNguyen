---
title: "Proposal"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

## 1. Project Summary

The project builds a cloud-based internship portal for students. The system allows students to create profiles, upload CVs, search for internship positions, and submit applications. Companies can publish internship posts, review applicants, and update application statuses. Administrators can manage users, approve internship posts, manage skills and job positions, and moderate community content.

The project goal is to create a complete web application with frontend, backend, database, file storage, authentication, logging, and a deployment path on AWS.

## 2. Problem

Students often search for internships across fragmented channels such as social media, email, company websites, and manual forms. This makes it difficult to track application status, manage CVs, and identify suitable opportunities.

For companies, receiving applications through multiple channels makes candidate screening, status updates, and feedback less centralized. For administrators, it is also difficult to control post quality, user accounts, and recruitment-market statistics.

Key problems:

- Lack of a centralized platform for students and companies.
- CVs and application data are not managed securely with role-based access.
- Internship post approval is not standardized.
- There is no dashboard for posts, applicants, skills, or popular job positions.
- Local-only deployment does not meet real operational requirements.

## 3. Solution

The proposed solution is a **Student Internship Portal** deployed as a web application on AWS:

- **ReactJS + Vite frontend** for student, company, and admin interfaces.
- **FastAPI backend** for REST APIs, business logic, and authorization.
- **JWT Authentication** to protect APIs and separate user roles.
- **Amazon RDS PostgreSQL** to store users, profiles, companies, internship posts, applications, skills, notifications, and forum data.
- **Amazon S3** to store CVs in a private bucket; the backend stores only object keys and generates short-lived presigned URLs for authorized users.
- **Amazon EC2** to run the FastAPI backend.
- **S3 Static Website Hosting or CloudFront** to serve the production frontend build.
- **CloudWatch Logs** to collect backend logs and support troubleshooting.

## 4. Solution Architecture

```text
User Browser
  -> React Frontend on S3/CloudFront
  -> FastAPI Backend on EC2
  -> Amazon RDS PostgreSQL
  -> Amazon S3 private bucket for CV files
  -> Amazon CloudWatch Logs
```

Main system flow:

1. A user registers or logs in.
2. The backend authenticates the account and returns JWT tokens.
3. A student updates their profile, uploads a CV, and applies to approved internship posts.
4. A company creates its profile, publishes internship posts, and reviews applicants.
5. An admin approves posts, manages users, skills, and job positions.
6. When an application or post status changes, the system creates a notification for the related user.

## 5. Benefits

- Centralizes internship searching and management.
- Improves transparency through clear application statuses.
- Protects CV files using a private S3 bucket and presigned URLs.
- Makes the database and backend easier to scale as usage grows.
- Fits the **Application Development on AWS** topic because it includes frontend, backend, database, storage, and monitoring.
