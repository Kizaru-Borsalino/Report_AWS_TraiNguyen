---
title: "Week 10 - RDS PostgreSQL"
date: 2024-01-01
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Goals

- Move the production database to Amazon RDS PostgreSQL.
- Connect the EC2 backend to RDS securely.

### Work Completed

| Day | Task | Start Date | Completion Date | Reference |
| --- | --- | --- | --- | --- |
| Day 1 | Create RDS PostgreSQL<br>Production database `internship_portal` | 2025-10-13 | 2025-10-13 | Amazon RDS Docs / Alembic Docs |
| Day 2 | Configure security group<br>Only EC2 backend can access port 5432 | 2025-10-14 | 2025-10-14 | Amazon RDS Docs / Alembic Docs |
| Day 3 | Update `DATABASE_URL`<br>Backend connects to RDS instead of SQLite | 2025-10-15 | 2025-10-15 | Amazon RDS Docs / Alembic Docs |
| Day 4 | Run Alembic migration<br>Create production schema | 2025-10-16 | 2025-10-16 | Amazon RDS Docs / Alembic Docs |

### Results

The database is separated from the backend server, which better matches cloud architecture. Alembic keeps the local and production schemas consistent.
