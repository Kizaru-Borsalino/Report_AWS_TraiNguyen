---
title: "Week 8 - Applicant listing, history flows, and data stability"
date: 2026-08-03
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Objectives

- Fix data issues that prevent companies from seeing applicants or candidates from seeing correct histories.
- Improve resume handling, application withdrawal, and re-apply behavior.
- Ensure application data stays consistent in RDS.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Fixed the applicant query per job so companies can see the correct submitted candidates. | 03/08/2026 | 03/08/2026 | [SQLAlchemy ORM Querying Guide](https://docs.sqlalchemy.org/en/20/orm/queryguide/index.html) |
| Tuesday | Added buttons to open profile details and download the submitted resume directly from the applicant card. | 04/08/2026 | 04/08/2026 | [Ant Design List](https://ant.design/components/list), [Ant Design Collapse](https://ant.design/components/collapse) |
| Wednesday | Enabled duplicate resume deletion, withdrawal, and re-application without corrupting history data. | 05/08/2026 | 05/08/2026 | [PostgreSQL Transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html), [SQLAlchemy Session Basics](https://docs.sqlalchemy.org/en/20/orm/session_basics.html) |
| Thursday | Standardized application statuses in Vietnamese and synchronized company and candidate views. | 06/08/2026 | 06/08/2026 | [State Machine Design Pattern](https://learn.microsoft.com/en-us/azure/architecture/patterns/state-machine), [Ant Design Tag](https://ant.design/components/tag) |
| Friday | Reviewed transactions and refresh behavior so status changes appear immediately after save. | 07/08/2026 | 07/08/2026 | [Amazon RDS best practices for PostgreSQL](https://docs.aws.amazon.com/prescriptive-guidance/latest/tuning-postgresql-parameters/introduction.html), [PostgreSQL Transactions](https://www.postgresql.org/docs/current/tutorial-transactions.html) |
| Saturday | Ran regression tests across company-admin-student flows on the AWS staging environment. | 08/08/2026 | 08/08/2026 | [Playwright Docs](https://playwright.dev/docs/intro), [Testing Pyramid](https://martinfowler.com/articles/practical-test-pyramid.html) |

### Outcomes

- Applicant lists and application histories became much more stable, reducing cross-role data issues.
- RDS now preserves business-state consistency across repeated updates.


