---
title: "Week 3 Worklog"
date: 28-09-2026
weight: 1
chapter: false
pre: "  1.3  "
---


### Week 3 Objectives:

* Understand and practice global content delivery optimization using Amazon CloudFront.
* Master the Serverless Compute model with AWS Lambda and build RESTful APIs using Amazon API Gateway.
* Understand and configure Domain Name System (DNS) resolution, routing management, and resource health checks using Amazon Route 53.
* Gain proficiency in monitoring, logging, and system auditing tools using Amazon CloudWatch & AWS CloudTrail.

### Tasks to be implemented this week:
| Day | Task                                                                                                                                                                                       | Start Date   | Completion Date | Resource Source                           |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| Mon | - Learn about Amazon CloudFront (Content Delivery Network - CDN) <br> - **Hands-on Practice:** <br>&emsp; + Create a CloudFront Distribution <br>&emsp; + Configure Origin (S3 Bucket or Custom Origin like EC2/ALB) <br>&emsp; + Configure Origin Access Control (OAC) to secure the S3 Bucket <br>&emsp; + Set up Caching policies, Behaviors, and HTTPS/SSL Certificates <br>&emsp; + Optimize content delivery and test Cache Invalidation <br>&emsp; + Clean up resources                                                                                             | 28/09/2026   | 28/09/2026      | <https://000008.awsstudygroup.com>
| Tue | - Learn about AWS Lambda & Serverless Compute <br> - **Hands-on:** <br>&emsp; + Create a Lambda Function using the AWS Console / CLI <br>&emsp; + Write and execute data processing scripts (Node.js / Python) <br>&emsp; + Configure automatic triggers from AWS services (S3, API Gateway, DynamoDB) <br>&emsp; + Configure Environment Variables & IAM Roles for Lambda permissions <br>&emsp; + Monitor and inspect activity logs via Amazon CloudWatch Logs <br>&emsp; + Clean up resources                                            | 29/09/2026   | 29/09/2026      | <https://000010.awsstudygroup.com> |
| 4   | - Learn about Amazon API Gateway (REST API & HTTP API) <br> - **Hands-on:** <br>&emsp; + Create an API Gateway (REST API / HTTP API) <br>&emsp; + Configure Resources, Methods (GET, POST, PUT, DELETE) & Integration Types <br>&emsp; + Integrate API Gateway with AWS Lambda Functions (Serverless Backend) <br>&emsp; + Configure CORS (Cross-Origin Resource Sharing) & Authentication / Authorization <br>&emsp; + Deploy API to Stages (Dev / Prod) & Test API calls <br>&emsp; + Clean up resources | 30/09/2026   | 30/09/2026      | <https://000011.awsstudygroup.com> |
| 5   | - Learn about Amazon Route 53 (Domain Name System - DNS) <br> - **Hands-on:** <br>&emsp; + Register a domain or configure a Hosted Zone on Amazon Route 53 <br>&emsp; + Create and manage DNS records (A, CNAME, MX, TXT) <br>&emsp; + Configure Routing Policies (Simple, Weighted, Latency-based, Failover, Geolocation) <br>&emsp; + Set up Route 53 Health Checks to monitor resource status <br>&emsp; + Integrate Route 53 with CloudFront / Application Load Balancer (ALB) / S3 Static Website <br>&emsp; + Clean up resources                  | 01/10/2026   | 01/10/2026      | <https://000060.awsstudygroup.com> |
| 6   | - Explore advanced Amazon Route 53 Routing Policies (Weighted, Latency-Based, Failover, Geolocation, Geoproximity, Multi-value Answer) <br> - **Hands-on practice:** <br>&emsp; + Initialize a multi-Region environment with EC2 / Application Load Balancer (ALB) <br>&emsp; + Configure Routing Policies to optimize traffic routing based on geography and latency <br>&emsp; + Set up Failover Routing Policy combined with Route 53 Health Checks for automatic redirection during system failures <br>&emsp; + Verify and test actual traffic routing <br>&emsp; + Clean up resources                                                                                         | 02/10/2026   | 02/10/2026      | <https://000061.awsstudygroup.com> | ### Week 3 Achievements:

* Optimized and secured content delivery via Amazon CloudFront:
  * Created and managed CloudFront distributions integrated with origins (S3 Bucket, ALB, or EC2). 
  * Secured S3 buckets using Origin Access Control (OAC) and configured optimal caching and behavior policies.

*   Built a serverless architecture using AWS Lambda & API Gateway:
  * Initialized functions, wrote data processing code (Node.js/Python), and assigned IAM roles to AWS Lambda. 
  * Configured automated triggers from AWS services and set up monitoring via CloudWatch Logs. 
  * Created REST APIs/HTTP APIs on Amazon API Gateway and integrated them with Lambda functions as a serverless backend. 
  * Configure CORS, Authentication/Authorization, and deploy APIs to environments (Dev/Prod).

* Domain management and network routing with Amazon Route 53:
  * Create Hosted Zones; register and manage DNS records (A, CNAME, MX, TXT). 
  * Master routing policies (Simple, Weighted, Latency-based, Failover, Geolocation) and configure Health Checks to monitor resources. 
  * Successfully integrate Route 53 with CloudFront, Load Balancers, and S3 static websites.

* System monitoring, alerting, and auditing with CloudWatch & CloudTrail:
  * Build CloudWatch Dashboards to track resource performance metrics.
  * Set up CloudWatch Alarms combined with Amazon SNS to automatically send alerts during incidents. 
  * Manage Log Groups, Log Streams, and Metric Filters; configure EventBridge for automated event handling. 
  * Enable AWS CloudTrail to log and audit all API activity within the account.

* Optimize costs by cleaning up resources after each practical exercise.