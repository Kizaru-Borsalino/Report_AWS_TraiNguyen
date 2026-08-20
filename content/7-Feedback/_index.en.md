---
title: "Sharing and Feedback"
date: 2026-08-16
weight: 7
chapter: false
pre: " <b> 7. </b> "
---

## Sharing

The most valuable thing I learned from JobGo is how product thinking and engineering thinking must work together. Before this project, I often approached software as a list of features to implement. During this internship, I learned to ask deeper questions: what does the user actually need, how should data move through the system, which states must be stored, and which role is allowed to act at each step. That shift in thinking helped me understand the project more clearly and reduced the amount of fragmented, reactive coding.

From a technical standpoint, JobGo gave me the chance to combine multiple areas into one coherent product: React frontend work, FastAPI backend design, database modeling, CV file handling, master data normalization, and AWS deployment planning. The most meaningful part is that I was not only implementing CRUD operations. I had to solve data synchronization problems across multiple roles and screens, which strengthened my understanding of state transitions, business flows, and API design for multi-actor systems.

From my perspective, the strongest part of the project is that it now contains a relatively complete recruitment workflow: guests can browse jobs publicly, candidates can build profiles and apply, companies can post jobs and review applicants, and administrators can manage reference data and approvals. In addition, the AI Matching Engine gives the platform a clearer identity beyond a basic job board.

At the same time, the project also exposed several weaknesses. When business scope expands quickly, both the UI and the data model can become fragmented unless the structure is planned early. Areas such as observability, CI/CD, rollback strategy, automated testing, and deeper matching intelligence still remain more directional than production-complete. This was an important realization for me: making a product run is only the first step; making it stable and scalable requires another layer of engineering discipline.

## Feedback

If I evaluate the project objectively, JobGo has reached a solid functional baseline, but it still has important gaps to address. The current matching engine is appropriate for an early-stage solution because it uses rule-based scoring over normalized data. However, in the long term it should evolve to handle richer and less predictable profile-job combinations. For example, when equivalent skills are written differently or when important job signals are implied in descriptions rather than fully represented by master data, the current logic becomes less flexible.

The second area for improvement is administration and operations. The system already supports admin, company, and candidate workflows, but a production-grade version would still need stronger automated tests, audit logging, deeper monitoring, tighter permission boundaries, and a repeatable deployment process. These concerns are less visible than user-facing features, but they directly influence long-term reliability and maintainability.

In the future, I would improve the project in three main directions. First, I would evolve AI Matching from a rule-based engine toward a more semantic approach, potentially using embeddings or meaning-based comparison when enough data becomes available. Second, I would introduce CI/CD pipelines and automated tests for the major workflows to reduce regression risk. Third, I would refine the user experience in data-heavy areas such as applicant lists, application history, and administrative reporting so that the system becomes not only functionally correct, but also easier to use in a realistic environment.
