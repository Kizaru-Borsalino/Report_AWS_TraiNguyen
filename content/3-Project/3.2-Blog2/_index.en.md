---
title: "Frontend Application"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

The frontend is built with **ReactJS + Vite** and provides separate interfaces for students, companies, and administrators.

## Frontend Structure

```text
frontend/
  src/
    api/
    components/
    hooks/
    pages/
    utils/
    main.jsx
    styles.css
  index.html
  package.json
```

## Page Groups

### Student

- `/student/home`: student dashboard.
- `/student/jobs`: internship list.
- `/student/companies`: company list.
- `/student/applications`: submitted applications.
- `/student/profile`: personal profile and CV.
- `/student/insights`: recruitment-market insights.
- `/student/forum`: community forum.

### Company

- `/company/home`: company dashboard.
- `/company/jobs`: internship post management.
- `/company/applicants`: applicant list.
- `/company/profile`: company profile.

### Admin

- `/admin/home`: overview dashboard.
- `/admin/users`: user management.
- `/admin/posts`: internship post approval.
- `/admin/job-positions`: job-position management.
- `/admin/skills`: skill management.
- `/admin/forum`: forum management.

## Backend Connection

The frontend calls APIs through `src/api/client.js`. In local development, it connects to the backend on port `8000`. In production, the `VITE_API_URL` environment variable points to the real API domain.

The frontend design focuses on clear workflows: role-based login, routing to the correct dashboard, displaying API data, and showing loading/error states to users.
