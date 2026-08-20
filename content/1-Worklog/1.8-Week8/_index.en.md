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
| Monday | Fixed the applicant query per job so companies can see the correct submitted candidates. | 03/08/2026 | 03/08/2026 | Applicant query review |
| Tuesday | Added buttons to open profile details and download the submitted resume directly from the applicant card. | 04/08/2026 | 04/08/2026 | Applicant card UX |
| Wednesday | Enabled duplicate resume deletion, withdrawal, and re-application without corrupting history data. | 05/08/2026 | 05/08/2026 | Resume/application consistency notes |
| Thursday | Standardized application statuses in Vietnamese and synchronized company and candidate views. | 06/08/2026 | 06/08/2026 | Status mapping table |
| Friday | Reviewed transactions and refresh behavior so status changes appear immediately after save. | 07/08/2026 | 07/08/2026 | RDS transaction checklist |
| Saturday | Ran regression tests across company-admin-student flows on the AWS staging environment. | 08/08/2026 | 08/08/2026 | Regression test suite |

### Outcomes

- Applicant lists and application histories became much more stable, reducing cross-role data issues.
- RDS now preserves business-state consistency across repeated updates.
