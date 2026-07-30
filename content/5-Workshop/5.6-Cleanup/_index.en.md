---
title : "Testing, Monitoring, and Cleanup"
date : 2024-01-01
weight : 6
chapter : false
pre : " <b> 5.6. </b> "
---

## 1. Post-deployment Testing

Final test flow:

1. Open the frontend domain.
2. Log in as a company.
3. Create a company profile.
4. Create an internship post.
5. Log in as an admin.
6. Admin approves the post.
7. Log in as a student.
8. Update the student profile.
9. Upload CV to S3.
10. Apply to the approved internship.
11. Company updates the application status.
12. Student checks the notification.

## 2. CloudWatch Logs

FastAPI writes logs to stdout/stderr. When running on EC2, CloudWatch Agent can send those logs to CloudWatch Logs.

Information to monitor:

- 4xx/5xx API errors.
- RDS connection errors.
- S3 upload or read errors.
- Health check frequency.
- EC2 CPU, RAM, and disk usage.

## 3. Cleanup

After the demo or workshop, unused resources should be cleaned up to avoid unexpected costs:

- Stop or terminate EC2 instance.
- Delete demo RDS if data does not need to be kept.
- Delete objects in the CV S3 bucket.
- Delete the demo frontend S3 bucket.
- Delete CloudWatch log groups if logs are no longer needed.
- Check the billing dashboard.

## 4. Workshop Conclusion

The workshop helped the team understand how to deploy a practical web application on AWS: backend on EC2, data in RDS, CV files in a private S3 bucket, frontend on static hosting, and logs monitored through CloudWatch.
