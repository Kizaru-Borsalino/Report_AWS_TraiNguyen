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
| Monday | Replaced the generic category master data with a job-level catalog such as Intern, Fresher, Junior, Middle, and Senior. | 10/08/2026 | 10/08/2026 | [Database normalization](https://www.ibm.com/think/topics/database-normalization), [Master data management overview](https://www.ibm.com/think/topics/master-data-management) |
| Tuesday | Added skills, desired position, location, work mode, employment type, and level to the student profile. | 11/08/2026 | 11/08/2026 | [Amazon Bedrock overview](https://aws.amazon.com/bedrock/), [Feature engineering](https://developers.google.com/machine-learning/data-prep/transform/feature-engineering) |
| Wednesday | Updated company forms to reuse the same master-data catalogs as the candidate side. | 12/08/2026 | 12/08/2026 | [OpenAPI Specification](https://swagger.io/specification/), [Pydantic Models](https://docs.pydantic.dev/latest/concepts/models/) |
| Thursday | Added input-validation rules to prevent free-text drift that would break scoring. | 13/08/2026 | 13/08/2026 | [Pydantic Validation](https://docs.pydantic.dev/latest/concepts/validators/), [OWASP Input Validation Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Input_Validation_Cheat_Sheet.html) |
| Friday | Reviewed the job and profile API responses to make them ready for matching results. | 14/08/2026 | 14/08/2026 | [REST API Design Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/api-design), [JSON:API Recommendations](https://jsonapi.org/recommendations/) |
| Saturday | Verified that candidate profile updates immediately change the matching inputs on AWS. | 15/08/2026 | 15/08/2026 | [Amazon Bedrock overview](https://aws.amazon.com/bedrock/), [AWS Well-Architected Reliability Pillar](https://docs.aws.amazon.com/wellarchitected/latest/reliability-pillar/welcome.html) |

### Outcomes

- The AI Matching inputs are now normalized and rich enough to calculate relevance.
- JobGo now has a clearer master-data foundation for both user experience and system logic.


