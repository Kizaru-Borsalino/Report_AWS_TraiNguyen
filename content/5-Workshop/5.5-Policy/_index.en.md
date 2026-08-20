---
title: "Security and policy"
date: 2026-08-11
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

- Only the backend can read and write to the resume bucket
- The public frontend serves static assets only
- RDS should not be public unless absolutely required
- Secrets must never be hard-coded in source code
- Logs should be sent to CloudWatch for incident tracing
