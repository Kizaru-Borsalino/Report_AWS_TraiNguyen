---
title : "Cài đặt backend trên EC2"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.4.2. </b> "
---

## Cài runtime

```bash
sudo apt update
sudo apt install -y python3 python3-venv python3-pip nginx
```

## Cài dependencies

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

## Cấu hình production environment

```env
ENVIRONMENT=production
DATABASE_URL=postgresql+psycopg2://app_user:<password>@<rds-endpoint>:5432/internship_portal
AWS_REGION=ap-southeast-1
S3_BUCKET_NAME=<your-cv-bucket>
BACKEND_CORS_ORIGINS=https://your-frontend-domain.com
```

## Chạy migration và seed data

```bash
alembic upgrade head
python seed.py
```

## Start backend

```bash
python -m uvicorn app.main:app --host 0.0.0.0 --port 8000
```

Trong production thực tế, backend nên được chạy bằng `systemd` để tự khởi động lại khi EC2 reboot hoặc process bị lỗi.
