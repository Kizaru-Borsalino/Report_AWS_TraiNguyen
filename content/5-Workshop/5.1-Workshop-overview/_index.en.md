---
title : "Architecture Overview"
date : 2024-01-01
weight : 1
chapter : false
pre : " <b> 5.1. </b> "
---

The workshop deploys the **Student Internship Portal** on AWS using a multi-component web application architecture.

## Main Components

```text
Browser
  -> React Frontend on S3/CloudFront
  -> FastAPI Backend on EC2
  -> Amazon RDS PostgreSQL
  -> Amazon S3 private bucket for CV files
  -> Amazon CloudWatch Logs
```
## Project architecture
![Architectural photos of the project](/images/cloud_aws_architec.png)


## Service Roles

- **Amazon EC2:** runs the FastAPI backend with Uvicorn.
- **Amazon RDS PostgreSQL:** stores business data such as users, profiles, companies, internship posts, applications, skills, notifications, and forum data.
- **Amazon S3:** stores CV files in a private bucket and can also host frontend static build files.
- **Amazon CloudFront:** distributes the frontend through HTTPS and improves access speed.
- **IAM Role:** grants the backend minimal access to S3.
- **Security Group:** controls traffic to EC2 and RDS.
- **CloudWatch Logs:** collects backend logs for troubleshooting and monitoring.

## CV Upload Flow

1. A student uploads a CV from the frontend.
2. The frontend sends the request to the FastAPI backend.
3. The backend checks authorization, file type, and file size.
4. The backend uploads the file to the private S3 bucket.
5. The database stores the object key.
6. When a company needs to view the CV, the backend generates a temporary presigned URL if the company is authorized.
