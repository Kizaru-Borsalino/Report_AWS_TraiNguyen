---
title: "AI Code Review with AWS Security Agent: Detecting Security Gaps Before Deployment"
date: 2026-07-03
weight: 2
chapter: false
pre: " <b> 3.2. </b> "
---

## Topic

**Series:** AWS Security Agent - Part 2  
**Published link:** [View Facebook post](https://www.facebook.com/groups/660548818043427?multi_permalinks=2228768907888069)

## Introduction

If the first article focused on security by design, this second post moves into the implementation stage. Its main point is simple but important: **an application that works functionally is not automatically secure**. Many vulnerabilities only become visible when the code is reviewed from the perspective of validation, authorization, authentication, and sensitive-data handling.

The article explains how **AI Code Review** with AWS Security Agent can help teams detect risks early, before code is merged or before the application reaches deployment.

## Main content

### 1. Why working code is not enough

The post starts with a familiar example: a login API behaves correctly, users submit email and password, the system authenticates them, and returns a JWT token. From a functional testing perspective, everything is fine.

However, from a security perspective, many questions remain:

- Is failed-login rate limiting in place?
- Does the JWT have a reasonable expiration time?
- Are passwords hashed using a proper algorithm?
- Does the API log sensitive information?
- Can attackers brute-force passwords through repeated attempts?

The article clearly distinguishes **functional correctness** from **security correctness**.

### 2. What AI Code Review means

In the post, I describe AI Code Review as the use of AI to:

- Analyze source code.
- Identify security risks.
- Explain why those risks matter.
- Suggest practical remediation steps.

Unlike tools that only enforce syntax or formatting rules, AI-assisted review tries to understand execution context, data flow, authentication logic, and authorization boundaries.

### 3. How AWS Security Agent supports review

The article outlines four main steps:

1. Read and analyze newly added or modified code.
2. Identify areas that may introduce security risk.
3. Explain the impact and root cause.
4. Suggest remediation or safer alternative code.

This helps developers address security issues during pull-request review instead of much later in the lifecycle.

### 4. JobGo-related examples

#### Login API

The article highlights a practical issue: if the system returns different error messages such as:

- "Email does not exist"
- "Wrong password"

an attacker can use that difference to enumerate valid accounts. A safer response would be:

- "Email or password is incorrect"

#### CV upload API

For the CV upload feature, the post raises important checks:

- Is file type restricted?
- Is file size limited?
- Is the filename normalized?
- Is the actual file content verified, or only its extension?

This is especially relevant to JobGo because students upload documents directly to the system.

#### Job-post management API

Another risk is checking only whether the user is authenticated, but not whether they truly own the job post they are modifying. Without ownership verification, one company could edit or delete another company’s posting.

### 5. The value of explanation, not only detection

One strong point made in the article is that AWS Security Agent does not merely say "this code is risky." It also explains:

- Why the issue is dangerous.
- What the potential impact is.
- How an attacker might exploit it.
- What remediation fits the application context.

This is especially useful for development teams that are still building secure-coding experience.

### 6. Lessons learned

The article concludes that features such as login, CV upload, and job-post management can all become attack surfaces if they are not protected properly. A system working as expected is never enough to guarantee that it is secure.

## Significance

This article helped reinforce the idea that security must be part of the software development lifecycle itself, especially during code review. That matters a lot in JobGo because the platform handles sensitive data such as accounts, resumes, candidate profiles, and recruitment information.

Writing this post also helped me convert abstract security theory into concrete examples. That made the learning process more practical and will help me review code more critically in future projects.

## References

- AWS Security Agent: <https://aws.amazon.com/vi/security-agent/>
