---
title: "Project Proposal"
date: 2026-06-29
weight: 2
chapter: false
pre: " <b> 2. </b> "
---

# JobGo on AWS

## Building an AI-assisted recruitment and job discovery platform on AWS

### 1. Executive Summary

**JobGo** is an online recruitment platform designed to help candidates find the right jobs faster and enable companies to evaluate applicants more efficiently. The system covers candidate profile management, company profile management, job posting, application submission, application-status tracking, centralized master-data administration, and an **AI Matching** engine that estimates the relevance between a candidate profile and a job post.

Rather than being treated as a local-only coursework system, the project is intentionally framed for **AWS production deployment** using:

- **Amazon CloudFront + Amazon S3** for the React frontend
- **Amazon ECS Fargate + Application Load Balancer** for the FastAPI backend
- **Amazon RDS for PostgreSQL** for relational data
- **A private Amazon S3 bucket** for resume storage
- **Amazon CloudWatch Logs** for monitoring and troubleshooting

### 2. Problem Statement

Modern hiring workflows typically suffer from three major pain points:

1. **Fragmented data**: candidates search for jobs across disconnected channels and struggle to track resumes and application states.
2. **Manual screening**: companies spend too much time reading profiles and manually estimating suitability.
3. **Lack of centralized governance**: without moderation, normalized reference data, and clear access control, platform quality deteriorates quickly.

JobGo addresses these issues through a centralized multi-role system with strong master-data governance and a relevance-scoring engine.

### 3. Proposed Solution

- Candidates can build profiles, upload resumes, browse jobs, view AI Matching, and track applications.
- Companies can maintain profiles, publish jobs, review applicants, and rank them by matching score.
- Administrators can approve jobs and manage the shared master-data catalog.

### 4. AWS Deployment Architecture

```text
User Browser
  -> CloudFront
  -> S3 static frontend
  -> Application Load Balancer
  -> ECS Fargate service (FastAPI backend)
  -> Amazon RDS PostgreSQL
  -> Amazon S3 private bucket (resume files)
  -> CloudWatch Logs / Alarms
```
![Architecture Diagram](/images/architecture_final.png)

### 5. Expected Outcome

- A working recruitment platform aligned with the intended business roles
- AI Matching that helps both candidates and companies make faster decisions
- A production-oriented AWS deployment model instead of a localhost-only setup
- Bilingual documentation suitable for demo, handover, and future extension
