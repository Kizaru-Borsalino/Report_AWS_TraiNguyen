---
title : "Test CV Upload"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.3.2. </b> "
---

## Test Flow

1. Log in to the frontend as a student.
2. Open the student profile page.
3. Select a valid CV file.
4. Send the upload request to the backend.
5. The backend stores the file in S3.
6. Check that a new object appears in the S3 bucket.
7. Log in as a company.
8. Open the applicant list and view the CV through a presigned URL.

## Success Criteria

- The CV cannot be accessed through a public URL.
- The backend stores the correct object key in the database.
- A presigned URL is generated only when the user is authorized.
- The URL expires after the configured duration, for example 300 seconds.

## Conclusion

S3 separates file storage from the backend server, reduces load on EC2, and matches cloud application storage requirements.
