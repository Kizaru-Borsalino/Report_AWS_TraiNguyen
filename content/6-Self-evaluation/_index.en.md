---
title: "Self-evaluation"
date: 2026-08-15
weight: 6
chapter: false
pre: " <b> 6. </b> "
---

## Achievements

Throughout the JobGo project, I made visible progress in three areas: business analysis, fullstack development, and AWS-oriented deployment thinking. At the beginning, I mainly approached the problem through isolated features such as registration, login, profile creation, or job posting. As the project evolved, I learned to see the product as a complete system that includes data structures, business workflows, access control, file storage, observability, and production deployment concerns.

From a technical perspective, I had the opportunity to work across the React frontend, FastAPI backend, and PostgreSQL database layer. I developed a better understanding of how to design APIs that support multiple actors such as guests, candidates, companies, and administrators. I also learned the importance of extracting shared master data instead of relying on uncontrolled free-text input, which improves consistency and provides a stronger foundation for the AI Matching Engine.

Another important achievement was the shift from local-only thinking to cloud deployment thinking. Even though some AWS deployment details in the report are presented as a production-oriented design rather than a fully live rollout, the research and design process helped me understand the role of Amazon S3, CloudFront, ECS Fargate, RDS PostgreSQL, and CloudWatch in a modern web architecture. This is one of the most meaningful improvements compared to my starting point at the beginning of the internship.

## Difficulties

The biggest challenge during JobGo was handling both business complexity and technical complexity at the same time. A recruitment platform is not only about posting jobs and applying to them. It also involves CV management, application status updates, job moderation, master data maintenance, and smooth coordination between candidate and company workflows. Many of the initial issues did not come from a single broken feature, but from weak synchronization between screens, data states, and role-specific actions.

The second major challenge was data modeling for AI Matching. If both candidate profiles and job postings allow too much uncontrolled free text, the system cannot calculate compatibility in a consistent way. That is why I had to revisit the model and normalize frequently used data such as skills, positions, locations, employment types, work modes, and levels into shared master data. This was time-consuming, but it significantly improved system consistency and future maintainability.

Another challenge was the bilingual report itself. Writing technical documentation in both Vietnamese and English while keeping the structure aligned with FCAJ expectations required a different kind of discipline. I realized that strong technical reporting is not easier than coding. It requires clarity, consistency, traceability, and the ability to turn implementation work into an organized narrative.

## Lessons Learned

The first lesson I learned is that business understanding must come before implementation speed. If actors, use cases, state transitions, and data responsibilities are not clear, the codebase will quickly become fragmented and repetitive. Once the business model is clear, database design, APIs, and UI behavior become much easier to reason about.

The second lesson is that normalized data is as important as processing logic. Before this project, I tended to focus on interface behavior and API delivery first. After JobGo, I understand that master data, validation rules, naming consistency, and workflow states are what determine whether a system remains stable as it grows. This is especially true for features like AI Matching, where input quality directly influences output quality.

The final lesson is that production thinking should begin at the earliest stages of development. A system may work in local development, but if security, logging, access control, file storage, scalability, and deployment concerns are not considered early, moving to a real environment becomes much harder. After this internship, I am more confident in viewing a web application not only as code, but as a product with a real deployment and operational lifecycle.
