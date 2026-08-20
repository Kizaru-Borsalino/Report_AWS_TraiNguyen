---
title: "Prepare the VPC, RDS, and private bucket"
date: 2026-08-08
weight: 1
chapter: false
pre: " <b> 5.4.1. </b> "
---

## Required Components

- 1 VPC with public subnets for the ALB and private subnets for ECS/RDS.
- 1 security group for the ALB and 1 security group for ECS.
- 1 [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html) instance for business data.
- 1 private bucket named `jobgo-resume-prod` for resumes and attachments.

## Design Notes

- The ALB receives Internet traffic, while ECS tasks only accept traffic from the ALB.
- RDS only allows inbound connections from the ECS security group.
- The resume bucket stays private; the backend exposes authorized downloads through pre-signed URLs or secure streaming.

## Main Data Tables

- `users`, `student_profiles`, `company_profiles`
- `jobs`, `applications`, `resumes`
- `skills`, `job_positions`, `levels`, `locations`, `employment_types`, `work_modes`

This model lets the AI matching logic compare normalized master data rather than free-form text.
