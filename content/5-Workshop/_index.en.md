---
title: "Workshop"
date: 2026-08-05
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

# Workshop

This section presents the **main technical project** of the report: deploying **JobGo** on AWS from end to end. Unlike the FCAJ sample workshop, the content below is tailored to the actual JobGo use case: a job portal with public visitors, candidates, companies, administrators, and an **AI Matching Engine** as the key differentiator.

## Goals

- Deliver the React frontend through **Amazon S3 + Amazon CloudFront**.
- Package the FastAPI backend as a container and run it on **Amazon ECS Fargate** behind an **Application Load Balancer**.
- Store relational data in **Amazon RDS for PostgreSQL**.
- Store resumes and attachments in a **private Amazon S3 bucket**.
- Observe the system with **Amazon CloudWatch Logs** and basic alarms.
- Reproduce how the **AI Matching score** is calculated from candidate profile master data and job master data.

## Workshop Content

1. [Architecture overview and deployment context](./5.1-Workshop-overview/)
2. [Prerequisites](./5.2-Prerequiste/)
3. [Frontend delivery with S3 and CloudFront](./5.3-S3-vpc/)
4. [Backend, database, and AI matching deployment](./5.4-S3-onprem/)
5. [Security, IAM, logging, and validation](./5.5-Policy/)
6. [Cleanup and handover](./5.6-Cleanup/)
