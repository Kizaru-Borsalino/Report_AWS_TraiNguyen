---
title: "Chu?n b? VPC, RDS v? private bucket"
date: 2026-08-08
weight: 1
chapter: false
pre: " <b> 5.4.1. </b> "
---

## Th?nh ph?n c?n t?o

- 1 VPC v?i public subnet cho ALB v? private subnet cho ECS/RDS.
- 1 security group cho ALB v? 1 security group cho ECS.
- 1 [Amazon RDS for PostgreSQL](https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html) cho d? li?u nghi?p v?.
- 1 private bucket `jobgo-resume-prod` cho CV v? file ??nh k?m.

## L?u ? thi?t k?

- ALB nh?n request t? Internet, c?n ECS task ch? nh?n traffic t? ALB.
- RDS ch? cho ph?p inbound t? security group c?a ECS.
- Bucket CV kh?ng public; backend t?o pre-signed URL ho?c stream file theo ph?n quy?n.

## C?c b?ng d? li?u ch?nh

- `users`, `student_profiles`, `company_profiles`
- `jobs`, `applications`, `resumes`
- `skills`, `job_positions`, `levels`, `locations`, `employment_types`, `work_modes`

Thi?t k? n?y gi?p AI matching kh?ng ph?i so s?nh text t? do m? d?a tr?n master data chu?n h?a.
