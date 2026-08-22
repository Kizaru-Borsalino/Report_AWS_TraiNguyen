---
title: "Week 2 - Backend foundation and authentication"
date: 2026-06-22
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---

### Objectives

- Complete the backend skeleton with FastAPI, SQLAlchemy, and migrations.
- Build registration, login, and role-based access for three user types.
- Prepare the PostgreSQL database design for the AWS environment.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Initialized the FastAPI app, settings, dependency injection, and router modules. | 22/06/2026 | 22/06/2026 | [FastAPI - Bigger Applications](https://fastapi.tiangolo.com/tutorial/bigger-applications/), [FastAPI Project Generation](https://fastapi.tiangolo.com/project-generation/) |
| Tuesday | Implemented the user schema, role enum, password hashing, and JWT authentication. | 23/06/2026 | 23/06/2026 | [FastAPI - OAuth2 with JWT](https://fastapi.tiangolo.com/tutorial/security/oauth2-jwt/) |
| Wednesday | Built registration APIs for students and companies and safely seeded the administrator account. | 24/06/2026 | 24/06/2026 | [OpenAPI Specification](https://swagger.io/specification/) |
| Thursday | Created the initial PostgreSQL migration and validated compatibility with Amazon RDS. | 25/06/2026 | 25/06/2026 | [Alembic Documentation](https://alembic.sqlalchemy.org/en/latest/), [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html) |
| Friday | Prepared IAM policies and parameter placeholders for database connection secrets on AWS. | 26/06/2026 | 26/06/2026 | [AWS IAM User Guide](https://docs.aws.amazon.com/IAM/latest/UserGuide/introduction.html), [AWS Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-parameter-store.html) |
| Saturday | Tested multi-role login flows and handled 401, 403, and validation errors. | 27/06/2026 | 27/06/2026 | [FastAPI Testing](https://fastapi.tiangolo.com/tutorial/testing/), [Postman API Testing](https://learning.postman.com/docs/tests-and-scripts/write-scripts/test-scripts/) |

### Outcomes

- The backend foundation became stable, supporting role-based access and future recruitment features.
- The data design is ready for Amazon RDS deployment without depending on a local-only setup.


