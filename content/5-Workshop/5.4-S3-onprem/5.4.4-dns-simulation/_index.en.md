---
title: "Deploy AI Matching and validate the end-to-end flow"
date: 2026-08-10
weight: 4
chapter: false
pre: " <b> 5.4.4. </b> "
---

## Matching logic

The first version of JobGo AI Matching does not rely on a generative model. Instead, it uses a weighted scoring formula on normalized master data:

- Skills
- Target position
- Level
- Location
- Employment type
- Work mode

Example:

```text
AI Match = Skill 40% + Position 20% + Level 15% + Location 10% + Job Type 10% + Work Mode 5%
```

## How the score is refreshed

- When a candidate updates the profile, the backend recalculates matching against open jobs.
- When the candidate opens a job detail page, the frontend requests the criterion-by-criterion breakdown.
- When a company opens the applicant list, the backend sorts candidates by matching score in descending order.

## Expected output

```text
AI Match: 96% - Highly compatible
Skills: 90%
Position: 100%
Level: 90%
Location: 100%
Job Type: 100%
Work Mode: 100%
Strong matches: Python, FastAPI, AWS
Missing: Docker, Redis
```

## End-to-end validation

1. A guest can browse jobs on the homepage but cannot see AI matching.
2. A candidate logs in, creates the profile, and sees the score refresh immediately after saving.
3. The candidate applies to the selected job and verifies the entry in the application history.
4. The company opens the correct job and sees applicants sorted by descending matching score.
5. The admin approves job postings and manages master data as standardized input for the matching engine.
