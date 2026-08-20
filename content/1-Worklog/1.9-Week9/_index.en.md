---
title: "Week 9 - Preparing normalized data for AI Matching"
date: 2026-08-10
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Objectives

- Add the missing candidate-profile fields required for matching.
- Restructure master data, especially job level and employment-type dimensions.
- Ensure the frontend and backend share the same normalized data model.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Replaced the generic category master data with a job-level catalog such as Intern, Fresher, Junior, Middle, and Senior. | 10/08/2026 | 10/08/2026 | Master data redesign notes |
| Tuesday | Added skills, desired position, location, work mode, employment type, and level to the student profile. | 11/08/2026 | 11/08/2026 | Matching field matrix |
| Wednesday | Updated company forms to reuse the same master-data catalogs as the candidate side. | 12/08/2026 | 12/08/2026 | Shared master data contract |
| Thursday | Added input-validation rules to prevent free-text drift that would break scoring. | 13/08/2026 | 13/08/2026 | Validation rules |
| Friday | Reviewed the job and profile API responses to make them ready for matching results. | 14/08/2026 | 14/08/2026 | API response design |
| Saturday | Verified that candidate profile updates immediately change the matching inputs on AWS. | 15/08/2026 | 15/08/2026 | Matching readiness checklist |

### Outcomes

- The AI Matching inputs are now normalized and rich enough to calculate relevance.
- JobGo now has a clearer master-data foundation for both user experience and system logic.
