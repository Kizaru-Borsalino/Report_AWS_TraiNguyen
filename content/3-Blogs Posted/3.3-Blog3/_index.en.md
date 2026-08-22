---
title: "Building AI Applications on AWS: What Do Developers Actually Need?"
date: 2026-07-04
weight: 3
chapter: false
pre: " <b> 3.3. </b> "
---

## Topic

**Published link:** [View Facebook post](https://www.facebook.com/groups/awsstudygroupfcj/permalink/2228769511221342/?rdid=BHSRlBz1EoDanLJa)

## Introduction

The third article expands beyond security and focuses on a broader topic: **building AI applications on AWS from a developer’s perspective**. The goal is not just to introduce a model, but to answer a practical question:

> If I want to build an AI application on AWS, what do I actually need to prepare?

The article argues that a complete AI application is much more than calling an LLM API. To make a system genuinely usable and production-ready, developers must also think about data, backend services, authentication, RAG, security, evaluation, monitoring, and deployment architecture.

## Main content

### 1. An AI application is not just a model

The article begins with the simplest mental model:

`User -> LLM -> Answer`

This is enough for an experiment, but not for a real product. In production, developers need to answer additional questions:

- Which model fits the use case?
- Where does the application’s private data live?
- How will the model use that data?
- How do we prevent unsafe or irrelevant output?
- How do we evaluate answer quality?
- How do we monitor the system in production?
- How will cost evolve as usage grows?

### 2. Foundation models and the role of Amazon Bedrock

The article presents **Amazon Bedrock** as a central AWS service for generative AI. Bedrock provides managed access to foundation models from multiple providers, so developers do not need to build and operate model infrastructure from scratch.

This enables a clearer architecture:

`Application -> Amazon Bedrock -> Foundation Model`

That matters because it lets developers focus more on the application layer and less on low-level AI infrastructure management.

### 3. What developers must understand about model selection

The post emphasizes that having access to a model does not mean every model is suitable. A real technical decision should consider:

- **Quality:** is the model good at the target task?
- **Latency:** does the application require real-time responses?
- **Cost:** do simple requests really need the largest model?
- **Context window:** how much information must be passed into the model?

This section pushes the discussion beyond demo chatbots into practical engineering trade-offs.

### 4. RAG and private application data

One of the most important ideas in the article is that **an LLM does not automatically know an organization’s internal data**. If we want to build an assistant for a university or company, we need a mechanism to inject private knowledge into the answer-generation process.

The article explains **RAG - Retrieval-Augmented Generation** through this flow:

`User Question -> Retrieve Relevant Information -> Relevant Context -> Foundation Model -> Generated Answer`

It then connects that idea to **Amazon Bedrock Knowledge Bases** as a managed RAG solution that reduces the amount of retrieval pipeline work developers must build themselves.

### 5. The six learning layers for developers

One of the most useful parts of the article is the six-layer learning roadmap:

#### Layer 1 - Application Developer

- HTML / CSS / JavaScript
- React or an equivalent framework
- REST API
- Backend
- Database
- Authentication

#### Layer 2 - AI Fundamentals

- LLMs
- Prompting
- Tokens
- Context
- Embeddings
- Inference

#### Layer 3 - Amazon Bedrock

- Foundation Models
- Model Invocation
- Prompting
- Knowledge Bases
- Guardrails

#### Layer 4 - RAG

- Documents
- Chunking
- Embeddings
- Retrieval
- Context
- Generation

#### Layer 5 - Production

- Security
- Evaluation
- Monitoring
- Logging
- Cost optimization

#### Layer 6 - Agentic AI

- Tools
- Agents
- Memory
- Multi-step workflows
- Agent evaluation
- Agent observability

### 6. Core message of the article

The central message is that building a real AI application requires system thinking. Developers should not begin by copying a chatbot tutorial and stop there. They need to understand the product layer, the data and AI layer, and the production cloud layer together.

## Significance

This article is especially meaningful because it connects directly to JobGo’s future direction, especially the **AI Matching** capability between candidate profiles and job postings. While writing it, I had the chance to reflect on what makes an AI feature truly useful: strong backend integration, normalized input data, master data quality, evaluation logic, and reliable AWS-based operations.

It also helped me realize that learning AI on AWS should follow a path from application fundamentals to production readiness, instead of focusing only on the model itself. That is a practical mindset for building real AI products with actual users.

## References

- Amazon Bedrock overview: <https://aws.amazon.com/bedrock/>
- What is Amazon Bedrock: <https://docs.aws.amazon.com/bedrock/latest/userguide/what-is-bedrock.html>
- Amazon Bedrock Knowledge Bases: <https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html>
- How Knowledge Bases work: <https://docs.aws.amazon.com/bedrock/latest/userguide/kb-how-it-works.html>
- AWS Training - Artificial Intelligence: <https://aws.amazon.com/training/learn-about/ai/>
- AWS Dev Hour - Learn Gen AI from Scratch: <https://aws.amazon.com/training/twitch/aws-dev-hour-learn-gen-ai-from-scratch/>
