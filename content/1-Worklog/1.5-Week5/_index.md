---
title: "Week 5 Worklog"
date: 12-10-2026
weight: 1
chapter: false
pre: "  1.5  "
---


### Week 5 Objectives:

* Start working with the team project.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                   | Start date | Completion date | Resource Source                            |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| 2 | - Identify the core concept for the project <br> - Group discussion, exchange of opinions and ideas among members <br> - Filter, evaluate, and select the final concept | 10/12/2026 | 10/12/2026 |
| 3 | - Brainstorm and establish the project direction <br> - Create a foundational framework for operations <br> - Preliminary task allocation among members | 10/13/2026 | 10/13/2026 |
| 4 | - Set up the backend using the AWS Console <br>&emsp; + API Gateway <br>&emsp; + Lambda | 10/14/2026 | 10/14/2026 |
| 5 | - Set up the backend using the AWS Console <br>&emsp; + Authentication requirements <br>&emsp; + Session ID | 10/15/2026 | 10/15/2026 |
| 6 | - Set up the backend using the AWS Console <br>&emsp; + Conversation history <br>&emsp; + Dynamic database <br>&emsp; + RAG invocation | 10/16/2026 | 10/16/2026 |

### Achievements for Week 5:

* Successfully created the Lambda function legal-ai-chat-lambda (Runtime: Python 3.12)
* Successfully created the REST API legal-ai-chat-api
* Created the /chat resource and a POST method with Lambda Proxy Integration
* Deployed the API to a staging stage and obtained an accessible endpoint URL
* Attached the AmazonDynamoDBFullAccess policy to the Lambda function's IAM role
* Updated the Lambda source code to include boto3 for reading from and writing to DynamoDB
* Updated the Lambda code to support the automatic generation of session_id and to handle GET /history/{session_id} requests
* Successfully created the /history/{session_id} resource with a GET method in API Gateway