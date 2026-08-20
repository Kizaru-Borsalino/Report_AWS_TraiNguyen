---
title: "Workshop Overview"
date: 2026-08-05
weight: 1
chapter: false
pre: " <b> 5.1. </b> "
---

## Context

JobGo is a multi-role recruitment platform serving guests, candidates, companies, and administrators. The challenge is not limited to UI and CRUD flows; it also requires:

- efficient frontend delivery,
- stable backend API runtime,
- secure resume storage,
- a clean separation between relational data and file storage,
- and operational visibility after deployment.

## Workshop goals

This workshop describes how to deploy JobGo on AWS in a basic production-oriented model:

- React frontend through **Amazon S3 + CloudFront**
- FastAPI backend through **Amazon ECS Fargate + ALB**
- relational data on **Amazon RDS PostgreSQL**
- resumes on a **private S3 bucket**
- logging and validation through **Amazon CloudWatch**

## High-level architecture

```text
User Browser
  -> CloudFront
  -> S3 static frontend
  -> Application Load Balancer
  -> ECS Fargate service (FastAPI backend)
  -> Amazon RDS PostgreSQL
  -> Amazon S3 private bucket (resume files)
  -> CloudWatch Logs / Alarms
```
