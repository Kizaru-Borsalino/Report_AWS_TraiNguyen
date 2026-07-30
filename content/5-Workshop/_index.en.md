---
title: "Workshop"
date: 2024-01-01
weight: 5
chapter: false
pre: " <b> 5. </b> "
---

This workshop focuses on the main cloud techniques used to move the project from a local environment to AWS. The content follows the project problem: building an internship portal with backend, frontend, database, private CV storage, and basic logging.

## Goals

- Deploy the FastAPI backend to Amazon EC2.
- Use Amazon RDS PostgreSQL instead of local SQLite.
- Store CV files in an Amazon S3 private bucket.
- Build the React frontend and deploy it to S3 Static Website Hosting or CloudFront.
- Configure IAM, Security Groups, CORS, and production environment variables.
- Monitor backend logs with Amazon CloudWatch Logs.

## Workshop Content

1. [Deployment Architecture Overview](5.1-Workshop-overview/)
2. [Preparing the AWS Environment](5.2-Prerequiste/)
3. [Configuring S3 for CV Storage](5.3-S3-vpc/)
4. [Deploying Backend and Database](5.4-S3-onprem/)
5. [IAM, Security, and Production CORS](5.5-Policy/)
6. [Testing, Monitoring, and Cleanup](5.6-Cleanup/)

## Deployment Architecture

```text
Browser
  -> S3 Static Website Hosting or CloudFront
  -> React frontend
  -> EC2 FastAPI backend
  -> RDS PostgreSQL
  -> S3 private bucket for CV files
  -> CloudWatch Logs
```
