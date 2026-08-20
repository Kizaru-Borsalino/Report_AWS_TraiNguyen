---
title: "Security và policy"
date: 2026-08-11
weight: 5
chapter: false
pre: " <b> 5.5. </b> "
---

- Chỉ backend mới có quyền đọc ghi bucket CV
- Frontend public chỉ phục vụ static assets
- RDS không mở public nếu không cần thiết
- Secrets không hard-code trong source code
- Log cần được thu về CloudWatch để truy vết khi có sự cố
