---
title: "Cloud Architect Competition Final"
date: 2026-07-11
weight: 1
chapter: false
pre: " <b> 4.1. </b> "
---

## Event Information

| Item | Details |
|---|---|
| Event name | **Cloud Architect Competition Final and two technology presentations** |
| Time | 09:00 - 12:00, July 11, 2026 |
| Location | 26th Floor, Bitexco Financial Tower |
| Role | Attendee |

## Event Image

![Cloud Architect Competition Final event image](/images/event1.jpg)

## Participation Summary

In this event, I attended the final round of the Cloud Architect competition, where the two strongest teams competed against each other. The competition was organized around multiple-choice questions related to AWS Cloud, system architecture, security, resource management, and practical deployment scenarios.

The teams had to answer 10 questions within a limited time while also choosing suitable strategies through support options such as **Double Points** and **Lowest Risk**. This made the competition not only a test of technical knowledge, but also a challenge of analysis, confidence assessment, and quick decision-making.

Through the competition, I realized that the role of a Cloud Architect is not limited to remembering AWS service names. A cloud architect needs to understand the purpose, strengths, limitations, and appropriate combinations of services in order to design systems with good performance, scalability, availability, security, and cost efficiency.

## AWS Security Sharing Session

Besides the competition, the event also included a sharing session about security on AWS. The session emphasized that cloud security should be considered as part of the architecture from the beginning, instead of being added only after the system has already been built.

One important topic was the **Shared Responsibility Model**. AWS is responsible for protecting the underlying cloud infrastructure, while users are responsible for configuring accounts, access permissions, data protection, network settings, and monitoring the activities of their own cloud resources.

### Account and Access Protection

The session reviewed basic IAM practices, including avoiding the use of the root account for daily tasks, enabling MFA for important accounts, granting permissions based on the principle of least privilege, and avoiding root access keys. These are simple steps, but they have a major impact on system security.

### Network Protection

The session also discussed how to use VPC and Security Groups to control network traffic. For a web application, only necessary ports such as HTTP/HTTPS should be opened, SSH access should be limited to trusted administrator IP addresses, and the database should be placed in a private subnet. The database Security Group should only allow connections from the backend instead of being exposed directly to the Internet.

### Data Protection

For data protection, configurations such as S3 Block Public Access, encryption at rest and in transit, and avoiding secrets in source code or GitHub repositories were highlighted. When running applications on EC2, IAM Roles should be used to grant AWS permissions instead of storing access keys directly on the server.

### Monitoring and Threat Detection

The event introduced several services that support monitoring and risk detection, including CloudTrail, GuardDuty, Security Hub, and AWS Shield Standard. CloudTrail helps track API activity history, GuardDuty supports abnormal behavior detection, Security Hub aggregates security findings, and Shield Standard provides basic DDoS protection for supported AWS services.

## Lessons Learned

After attending the event, I gained a clearer understanding of how a Cloud Architect thinks when designing systems on AWS. A good architecture needs to balance performance, security, scalability, reliability, and operating cost.

The AWS Security session also helped me understand that basic security configurations such as IAM, MFA, Security Groups, S3 Block Public Access, and log monitoring are essential foundations when deploying any application to the cloud. These lessons directly support our project when designing and deploying the backend, database, and file storage components on AWS.
