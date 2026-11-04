---
title : "Security and operations"
date : 15-10-2026
weight : 6 
chapter : false
pre : "  5.6  "
---

#### Overview

| Item | Content |
| ---- | ------- |
| Purpose | Know the current security posture, monitor behavior and cost, and plan improvements |
| AWS services | CloudWatch, AWS Budgets, IAM |

#### 5.6.1. Current security status

| Area | Current state | Risk | Recommendation |
| ---- | ------------- | ---- | -------------- |
| API Gateway | Public, no authentication | Anyone with the URL can call it and use up the Groq quota | Throttling + usage plan / API key; Cognito later |
| CORS | Access-Control-Allow-Origin: * | Any website can call the API from a browser | Restrict to the S3 site origin after the demo |
| Groq API key | Lambda environment variable | Exposed if committed or screenshotted | Move to SSM Parameter Store (SecureString); rotate if leaked |
| S3 website | Public read, HTTP only | Traffic is not encrypted | Put CloudFront in front for HTTPS if needed |
| Data sent to Groq | Questions leave AWS | Real customer data could leak outside the account | Sample questions only; review Groq's data policy; consider Bedrock |
| CloudWatch | Lambda logs enabled | Logs may contain user questions | Set retention (7-14 days); avoid logging sensitive text |

#### 5.6.2. Monitoring and cost control

**Goal**

Detect errors and unexpected cost early.

**Steps**
1. Set a log retention period on the Lambda log group.
2. Create an alarm for Lambda errors (optional).
3. Check the Billing Free Tier usage page regularly and keep the Budget alert from 5.2.

[ INSERT SCREENSHOT ]

CloudWatch log group / alarm

5.6-Security/cloudwatch-dashboard.png

**Verify**

A test request appears in the logs; the Budget alert is active.

#### 5.6.3. Hardening roadmap

1. Add API throttling and a usage plan to protect the Groq quota (high priority, no code change in the frontend).
2. Move the Groq key to SSM Parameter Store and grant Lambda read access to that one parameter.
3. Restrict CORS to the website origin.
4. Add Cognito sign-in if the system leaves demo mode.
5. Test: call the API at high speed and confirm throttling; try prompt-injection questions; scan the repository for secrets.

[ INSERT SCREENSHOT ]
Security test results
5.6-Security/pentest.png