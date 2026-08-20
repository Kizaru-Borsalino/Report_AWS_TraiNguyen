---
title: "Week 10 - Building the AI Matching Engine"
date: 2026-08-17
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Objectives

- Implement the relevance engine that scores candidate profiles against job descriptions.
- Expose AI Matching to candidates on the job board and to companies on the applicant list.
- Rank applicants by match score to accelerate hiring decisions.

### Tasks Completed

| Day | Task | Start date | End date | References |
| --- | --- | --- | --- | --- |
| Monday | Designed a weighted scoring formula for skills, position, level, location, employment type, and work mode. | 17/08/2026 | 17/08/2026 | Matching formula notes |
| Tuesday | Built a backend service returning the overall score, qualitative label, matched skills, and missing skills. | 18/08/2026 | 18/08/2026 | Matching service contract |
| Wednesday | Attached matching results to the public jobs API for signed-in candidates with completed profiles. | 19/08/2026 | 19/08/2026 | Public jobs API integration |
| Thursday | Displayed a highlighted AI Matching badge in job cards and detailed job drawers. | 20/08/2026 | 20/08/2026 | Frontend matching UI |
| Friday | Sorted company applicant lists by descending match score. | 21/08/2026 | 21/08/2026 | Applicant ranking logic |
| Saturday | Verified that profile updates refresh matching scores immediately without requiring re-login. | 22/08/2026 | 22/08/2026 | Matching refresh test plan |

### Outcomes

- The AI Matching Engine became the flagship capability of JobGo.
- Companies can prioritize strong candidates, while students receive quantitative feedback before applying.
