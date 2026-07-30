---
title : "Install Backend on EC2"
date : 2024-01-01
weight : 2
chapter : false
pre : " <b> 5.4.2. </b> "
---

## Install Runtime

```bash
sudo apt update
sudo apt install -y python3 python3-venv python3-pip nginx
```

## Install Dependencies

```bash
cd backend
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

## Configure Production Environment

```env
ENVIRONMENT=production
DATABASE_URL=postgresql+psycopg2://app_user:<password>@<rds-endpoint>:5432/internship_portal
AWS_REGION=ap-southeast-1
S3_BUCKET_NAME=<your-cv-bucket>
BACKEND_CORS_ORIGINS=https://your-frontend-domain.com
```

## Run Migration and Seed Data

```bash
alembic upgrade head
python seed.py
```

## Start Backend

```bash
python -m uvicorn app.main:app --host 0.0.0.0 --port 8000
```

In a real production environment, the backend should run with `systemd` so it can restart automatically after EC2 reboots or process failures.
