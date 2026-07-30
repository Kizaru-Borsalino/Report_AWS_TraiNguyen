---
title : "Triển khai backend và database"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4. </b> "
---

## 1. Tạo RDS PostgreSQL

Thông số đề xuất cho demo:

```text
Engine: PostgreSQL
DB name: internship_portal
Username: app_user
Public access: No
Storage: 20 GB
Backup: Enabled
```

Security group của RDS chỉ cho phép inbound PostgreSQL port `5432` từ security group của EC2 backend.

## 2. Tạo EC2 backend

Thông số đề xuất:

```text
OS: Ubuntu LTS
Instance type: t3.micro hoặc t3.small
Inbound:
  22 từ IP cá nhân
  80/443 từ internet nếu dùng Nginx
  8000 chỉ mở tạm thời để test
```

## 3. Cài runtime

```bash
sudo apt update
sudo apt install -y python3 python3-venv python3-pip nginx
```

## 4. Chạy backend

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
alembic upgrade head
python seed.py
python -m uvicorn app.main:app --host 0.0.0.0 --port 8000
```

## 5. Kiểm tra

Health endpoint:

```text
GET /health
```

Kết quả mong đợi:

```json
{
  "status": "ok",
  "service": "Student Internship Portal"
}
```
