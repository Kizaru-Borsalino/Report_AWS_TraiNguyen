---
title : "Test Backend API"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.4.3. </b> "
---

## Health Check

Open the endpoint:

```text
http://<ec2-public-ip>:8000/health
```

Expected result:

```json
{
  "status": "ok",
  "service": "Student Internship Portal"
}
```

## Swagger Docs

FastAPI automatically provides API documentation at:

```text
http://<ec2-public-ip>:8000/docs
```

## Main Flow Testing

1. Log in with a demo account.
2. Company creates an internship post.
3. Admin approves the post.
4. Student uploads CV and applies.
5. Company updates the application status.
6. Check the student's notification.

## Result

If the endpoints work correctly, the backend can connect to RDS, read and write data successfully, and process the main business flow of the project.
