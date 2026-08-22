---
title: "References"
date: 2026-08-17
weight: 8
chapter: false
pre: " <b> 8. </b> "
---

This section summarizes the materials used during the analysis, implementation, and AWS-oriented deployment planning of JobGo. These references were used not only for report writing, but also for architecture design, API development, frontend implementation, file storage strategy, and business data normalization.

| Document Group | Document Name | Link | Usage Purpose |
| --- | --- | --- | --- |
| AWS | AWS Well-Architected Framework | https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html | Used to understand how to evaluate the architecture across security, reliability, performance, and cost optimization dimensions. |
| AWS | Amazon S3 User Guide | https://docs.aws.amazon.com/AmazonS3/latest/userguide/Welcome.html | Used to study frontend static asset hosting, private resume storage, and controlled file access patterns. |
| AWS | Amazon CloudFront Developer Guide | https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/Introduction.html | Referenced for CDN-based frontend delivery, caching strategy, HTTPS support, and SPA routing behavior. |
| AWS | Amazon ECS Developer Guide | https://docs.aws.amazon.com/AmazonECS/latest/developerguide/Welcome.html | Used to describe the container-based deployment direction for the FastAPI backend on ECS Fargate. |
| AWS | Amazon RDS for PostgreSQL Documentation | https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_PostgreSQL.html | Referenced for relational data storage planning for users, profiles, jobs, and applications. |
| AWS | Amazon CloudWatch Documentation | https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/WhatIsCloudWatch.html | Used in the logging, alarm, monitoring, and production observability sections of the report. |
| AWS | IAM Best Practices | https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html | Referenced for least-privilege access design, secret handling, and AWS resource protection. |
| Backend | FastAPI Documentation | https://fastapi.tiangolo.com/ | Used to design APIs, request and response validation, and backend service structure. |
| Backend | SQLAlchemy Documentation | https://docs.sqlalchemy.org/ | Referenced for model mapping, database interaction, and PostgreSQL ORM integration. |
| Backend | Pydantic Documentation | https://docs.pydantic.dev/ | Used for schema definition, input validation, and API payload normalization. |
| Backend | Uvicorn Documentation | https://www.uvicorn.org/ | Referenced for serving the ASGI application in development and production-like scenarios. |
| Frontend | React Documentation | https://react.dev/ | Used to structure multi-role interfaces, stateful pages, and frontend business flows. |
| Frontend | Vite Guide | https://vite.dev/guide/ | Referenced for frontend build flow, environment configuration, and static asset generation. |
| Frontend | Ant Design Documentation | https://ant.design/docs/react/introduce | Used to select reusable UI components and standardize the frontend interaction model. |
| Frontend | Ant Design Icons | https://ant.design/components/icon | Referenced for free icon resources used across JobGo screens and major actions. |
| Technical Documentation | Hugo Documentation | https://gohugo.io/documentation/ | Used to structure the internship report website, bilingual content layout, and site build process. |
| Technical Documentation | GitHub Pages Documentation | https://docs.github.com/en/pages | Referenced for publishing the report website and understanding the deployment flow. |
| Report / Requirements | FCAJ Project Rules | https://hcm-rules.awsfcaj.com/3-project/ | Used as the official guideline for report structure, worklogs, workshop content, blog requirements, and expected deliverables. |
| Report / Requirements | Workshop Sample | https://workshop-sample.awsfcaj.com/5-workshop/ | Used as a structural reference for the workshop chapter before adapting it to the JobGo project context. |
| Source code | Project_AWS_Trai_JobGo | https://github.com/Kizaru-Borsalino/Project_AWS_Trai_JobGo | Source code of the practical project used in this report.|
| Video demo | VideoDemo_Jobgo | https://drive.google.com/drive/folders/1XVq1LOzE-sm1OYaa7ji7e_abpZ6v5QGi?usp=sharing
drive.google.com | Demo video showing the main project workflow and features.|