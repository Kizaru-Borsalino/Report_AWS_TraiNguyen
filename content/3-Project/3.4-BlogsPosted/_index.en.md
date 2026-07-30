---
title: "Blogs Posted"
date: 2026-07-29
weight: 4
chapter: false
pre: " <b> 3.4. </b> "
---

## Overview

During the project, the team not only built a practical application but also summarized the learning process into technical blog posts. These posts helped organize the analysis, solution design, backend/frontend implementation, and use of AWS services in the project.

## Blog List

| Blog | Topic | Main Content | Learning Value | Link |
| --- | --- | --- | --- | --- |
| Blog 1 | Building Secure Applications from the Design Phase with AWS Security Agent | Explains why security should be considered during system design, introduces AWS Security Agent, Threat Modeling, and applies the ideas to the Student Internship Portal project. | Learned the "Design for Security" mindset, how to identify architectural risks early, and how to improve AWS deployments more securely. | To be updated |
| Blog 2 | Backend API and Database Design | Describes how the backend was built with FastAPI and how the Auth, Student, Company, Admin, Internship, Analytics, and Forum modules were designed. | Strengthened knowledge of REST APIs, role-based authorization, database design, and backend business logic. | To be updated |
| Blog 3 | Deploying the Project on AWS | Summarizes how the backend was deployed on EC2, how RDS PostgreSQL was used for the database, how S3 stored CV files, and how CloudWatch supported log monitoring. | Understood the process of moving an application from local development to the cloud and the key points to consider during deployment. | To be updated |

## Blog 1 - Building Secure Applications from the Design Phase with AWS Security Agent

The first blog post belongs to the **AWS Security Agent** series. It focuses on the idea that security should not only start after an application has been completed. A secure design from the beginning can help development teams identify and remove many risks before they become vulnerabilities in source code or deployment environments.

The post emphasizes that many security issues do not come directly from programming mistakes, but from early architectural decisions. For example, a database may be placed in a network area that is reachable from the Internet, an API may lack a proper authentication mechanism, or AWS services may receive permissions beyond their actual needs. If these issues are discovered only after the system is complete, fixing them often requires more time and cost.

### AWS Security Agent

The blog introduces **AWS Security Agent** as an AI assistant that helps development teams evaluate the security of a system from the design phase. Instead of only scanning source code, Security Agent can analyze design documents, architecture diagrams, data flows, AWS deployment configurations, and relationships between services.

From this information, the tool can help identify potential security risks and suggest improvements before the team starts coding or deploying the system. This represents a shift in mindset from **Fix Security** to **Design for Security**.

### Threat Modeling

An important part of the post is **Threat Modeling**, which is the process of analyzing a system to identify potential threats. It helps answer questions such as what the system needs to be protected from, which components are most exposed, how an attacker might exploit the system, and what design changes are needed to reduce risk.

AWS Security Agent does not replace security experts, but it can help development teams detect architectural problems earlier before they become real vulnerabilities in the product.

### Connection to the Student Internship Portal Project

The blog applies these ideas to the **Cloud-based Student Internship Portal on AWS** project. The system uses services such as Amazon CloudFront, Amazon S3, Amazon EC2, Amazon RDS PostgreSQL, AWS IAM, and Amazon CloudWatch. From a security perspective, the team needs to consider whether RDS is placed in a private subnet, whether EC2 exposes SSH to the entire Internet, whether IAM Roles have excessive permissions, and whether data exchanged between components is encrypted.

One practical example is deploying Amazon RDS with public access enabled for convenience during development. Functionally, the system may still work normally, but from a security perspective, this introduces significant risk. AWS Security Agent can recommend placing RDS in a private subnet, allowing access only from EC2 through Security Groups, and removing direct access from the Internet.

### Key Takeaways

Through this blog post, I learned that a good architecture is not only one that works correctly, but also one that is secure, controllable, and able to reduce risks early. Evaluating security from the design phase helps reduce remediation cost, supports developers in understanding the impact of architectural decisions, and establishes a foundation for DevSecOps thinking in later development stages.

Reference: [AWS Security Agent](https://aws.amazon.com/vi/security-agent/)

## Lessons Learned

Writing blog posts gave me an opportunity to review the whole project in a more structured way. Instead of only focusing on code, I had to explain the problem, the reason for choosing each technology, how the components connected with each other, and the results achieved after implementation.

This activity helped me improve technical communication, documentation writing, information selection, and the ability to explain a technology solution in a clearer way for readers.
