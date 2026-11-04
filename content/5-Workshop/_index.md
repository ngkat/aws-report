---
title: "Workshop"
date: 15-10-2026
weight: 5
chapter: false
pre: " <b> 5. </b> "
---


# AI Legal & Security Assistant
Serverless RAG for Legal & Data Protection Compliance on AWS

#### Overview

AI Legal & Security Assistant is a preliminary legal-consultation assistant for businesses, focused on Decree 13/2023/ND-CP (personal data protection). Employees type a question or a real scenario; the system looks up relevant legal articles in a database, then a large language model analyzes the question using only those articles.

The system is not a lawyer and does not produce official legal conclusions. If the database lacks a basis, the system must say so.

The system is built on a serverless architecture with these components:
* Interface – static web page (index.html) hosted on Amazon S3 static website hosting
* API – Amazon API Gateway (CORS and standardized errors)
* Backend – AWS Lambda (Python): retrieves legal articles and calls the LLM
* Knowledge base – Amazon DynamoDB (table LegalArticles)
* LLM – Groq API (qwen/qwen3.8-27b), an external service outside AWS
* Monitoring – Amazon CloudWatch

![alt text](<../images/Architecture and data-flow diagram.png>)

Architecture and data-flow diagram

#### Content

1. [Introduction](5.1-Introduction/)
2. [Prerequiste](5.2-Prerequiste/)
3. [Phase 1 – Prompt setup and RAG mechanism](<5.3-Phase 1 – Prompt setup and RAG mechanism>)
4. [Phase 2 – Backend: from database to Lambda and API](<5.4-Phase 2 – Backend from database to Lambda and API>)
5. [Frontend – S3 static website](<5.5-Frontend – S3 static website>)
6. [Security & operations](<5.6-Security & operations>)
7. [Final output and next steps](<5.7-Final output and next steps>)
8. [Clean up](5.6-Cleanup/)