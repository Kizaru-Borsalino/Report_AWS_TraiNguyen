---
title: "Backend API"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

The backend is built with **FastAPI**. It provides APIs for the frontend, handles business logic, authenticates users, and connects to the database.

## Backend Structure

```text
backend/
  app/
    routers/
      auth.py
      student.py
      company.py
      admin.py
      internships.py
      analytics.py
      forum.py
      common.py
    main.py
    models.py
    schemas.py
    database.py
    config.py
    auth.py
    services.py
  alembic/
  tests/
  requirements.txt
```

## Main Modules

- **Auth:** registration, login, current-user lookup, and refresh token handling.
- **Student:** student profile management, CV upload, and application lookup.
- **Company:** company profile, internship posts, applicant lists, and application status updates.
- **Admin:** user management, post approval, skills, job positions, and forum moderation.
- **Internships:** public list of approved internship positions.
- **Analytics:** statistics for skills, positions, locations, and salary ranges.
- **Forum:** professional communities, posts, comments, likes, and saved posts.

## Database

Main tables include:

- `users`
- `student_profiles`
- `companies`
- `internship_posts`
- `job_positions`
- `applications`
- `skills`
- `notifications`
- `forum_categories`
- `forum_posts`
- `forum_comments`
- `forum_likes`
- `forum_saves`

The backend uses SQLite for local development and PostgreSQL on Amazon RDS for production. The schema is managed through Alembic migrations so changes can be applied consistently across environments.

## Security and Authorization

The system has three user roles: `student`, `company`, and `admin`. Each API is protected according to its required role to prevent users from accessing data or actions outside their permissions.

CV files are not stored directly in the database. Files are stored in a private S3 bucket, and the database stores only object keys or storage references. When an authorized user needs to view a CV, the backend generates a short-lived presigned URL.
