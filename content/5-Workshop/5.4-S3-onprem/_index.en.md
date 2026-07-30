---
title : "Deploying Backend and Database"
date : 2024-01-01
weight : 4
chapter : false
pre : " <b> 5.4. </b> "
---

## 1. Create RDS PostgreSQL

Recommended demo settings:

```text
Engine: PostgreSQL
DB name: internship_portal
Username: app_user
Public access: No
Storage: 20 GB
Backup: Enabled
```

The RDS security group should allow inbound PostgreSQL port `5432` only from the backend EC2 security group.

## 2. Create Backend EC2

Recommended settings:

```text
OS: Ubuntu LTS
Instance type: t3.micro or t3.small
Inbound:
  22 from personal IP
  80/443 from internet if using Nginx
  8000 only temporarily for testing
```

## 3. Install Runtime

```bash
sudo apt update
sudo apt install -y python3 python3-venv python3-pip nginx
```

## 4. Run Backend

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
alembic upgrade head
python seed.py
python -m uvicorn app.main:app --host 0.0.0.0 --port 8000
```

## 5. Check

Health endpoint:

```text
GET /health
```

Expected result:

```json
{
  "status": "ok",
  "service": "Student Internship Portal"
}
```
