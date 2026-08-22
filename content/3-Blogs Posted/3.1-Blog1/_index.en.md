---
title: "Building Secure Applications from the Design Stage with AWS Security Agent"
date: 2026-07-02
weight: 1
chapter: false
pre: " <b> 3.1. </b> "
---

## Topic

**Series:** AWS Security Agent - Part 1  
**Published link:** [View Facebook post](https://www.facebook.com/groups/660548818043427?multi_permalinks=2227782947986665)

## Introduction

This article focuses on a key principle in modern software engineering: **security should not start after the application is finished, but from the architecture and design stage**. Instead of waiting until deployment to check for vulnerabilities, the post explains why teams should think about network boundaries, access control, and data flow protection from the beginning.

It introduces **AWS Security Agent** as an AI-assisted helper that can support development teams in reviewing system design before writing code or deploying the architecture in practice.

## Main content

### 1. Why security must start from design

Development teams often prioritize features, performance, and delivery speed. However, many serious risks do not come from minor coding mistakes. They come from initial design decisions, such as:

- Databases being exposed to the Internet.
- Application servers opening unnecessary ports.
- Internal and public APIs not being separated.
- Sensitive data processing components lacking isolated protection zones.
- IAM permissions being broader than required.

If such issues are found only after implementation, the cost of fixing them is much higher because they affect architecture, network layout, and operational controls.

### 2. What AWS Security Agent contributes

In the article, AWS Security Agent is presented as an AI-powered security assistant that can help analyze:

- System design documents.
- Architecture diagrams.
- Data flows between components.
- AWS deployment configurations.
- Access relationships across services.

This shifts the mindset from **"fixing security later"** to **"designing for security first."**

### 3. Threat modeling as a practical review method

One of the main concepts covered in the post is threat modeling. I described it as a process of answering four questions:

1. What threats must the system be protected against?
2. Which components are likely targets?
3. How could attackers exploit the system?
4. What design changes can reduce those risks?

AWS Security Agent is positioned as a supporting tool that helps developers identify architectural weaknesses before they become real product vulnerabilities.

### 4. Connection to the JobGo project

The article then links this idea directly to the JobGo architecture, which includes:

- Amazon CloudFront
- Amazon S3
- Amazon EC2
- Amazon RDS PostgreSQL
- AWS IAM
- Amazon CloudWatch

From that architecture, the post raises practical security questions such as:

- Is Amazon RDS deployed in a private subnet?
- Is SSH on EC2 open to the whole Internet?
- Is CloudFront the only public access path, or can users reach the server directly?
- Does the EC2 IAM role have excessive permissions?
- Is traffic between components encrypted?

### 5. Example discussed in the article

One strong example is the case where Amazon RDS is configured as publicly accessible during development for convenience. Functionally, the system still works, but from a security perspective it introduces unnecessary exposure. The article explains improvements such as:

- Moving RDS into a private subnet.
- Restricting database access to EC2 through security groups.
- Removing direct Internet access.
- Separating the application tier and the data tier clearly.

### 6. Benefits of early security review

The article concludes that reviewing security at the design stage helps teams:

- Reduce rework cost.
- Build safer architecture.
- Support developers who are not security specialists.
- Establish a better foundation for DevSecOps practices.

## Significance

This article was important for me in two ways.

First, it helped me view JobGo not only as a functional web platform, but as a cloud system that needs deliberate protection decisions.

Second, writing it reinforced the idea that effective security is rarely about late fixes. It is mostly about making sound design choices early. That mindset will be highly valuable in future AWS-based or production-grade systems.

## References

- AWS Security Agent: <https://aws.amazon.com/vi/security-agent/>
