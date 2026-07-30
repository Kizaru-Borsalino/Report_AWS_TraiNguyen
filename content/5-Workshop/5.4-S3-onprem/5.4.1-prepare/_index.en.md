---
title : "Prepare EC2 and RDS"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.4.1. </b> "
---

## RDS PostgreSQL

Create a production database with recommended settings:

```text
Engine: PostgreSQL
DB name: internship_portal
Username: app_user
Public access: No
Storage: 20 GB
```

The RDS security group should open port `5432` only to the backend EC2 security group.

## Backend EC2

Create an EC2 instance using Ubuntu LTS. Configure inbound rules:

```text
22: from personal IP for SSH
80/443: from internet if using Nginx/HTTPS
8000: only temporarily during testing
```

After creating EC2, attach an IAM Role with minimum permission to the CV S3 bucket.

## Result

The cloud environment has a backend server, a separate database, and network rules that allow the backend to connect to RDS.
