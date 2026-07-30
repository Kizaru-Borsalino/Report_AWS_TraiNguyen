---
title : "Configuring S3 CV Storage"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.3. </b> "
---

Amazon S3 is used to store student CV files. Because CVs contain personal data, the bucket must be private.

## 1. Create Bucket

Recommended settings:

```text
Bucket purpose: CV uploads
Region: ap-southeast-1
Block public access: On
Encryption: SSE-S3 or SSE-KMS
Versioning: Optional
```

## 2. Grant Backend Permission

The backend on EC2 only needs minimal permissions to upload and read CV files:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "s3:PutObject",
        "s3:GetObject"
      ],
      "Resource": "arn:aws:s3:::<your-cv-bucket>/*"
    }
  ]
}
```

## 3. Configure Backend

```env
AWS_REGION=ap-southeast-1
S3_BUCKET_NAME=<your-cv-bucket>
S3_PRESIGNED_URL_EXPIRE_SECONDS=300
```

## 4. Test

1. Log in as a student.
2. Update the student profile.
3. Upload a CV.
4. Check whether the object appears in the S3 bucket.
5. Log in as a company and open the applicant CV through the backend API.

The expected result is that the CV is not publicly accessible, but authorized users can view it through a presigned URL.
