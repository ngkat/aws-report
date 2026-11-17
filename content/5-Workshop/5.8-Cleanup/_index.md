---
title : "Clean up"
date : 15-10-2026
weight : 6
chapter : false
pre : "  5.6  "
---

#### Delete resources in the following order to avoid dependency errors and unnecessary costs:

1: S3 bucket `ai-legal-assistant-frontend-hau`.
![alt text](../../images/clean_up_1.png)
2: API in API Gateway.
![alt text](../../images/clean_up_2.png)
3: Lambda function and its associated CloudWatch log group.
![alt text](../../images/clean_up_3.png)
![alt text](../../images/clean_up_4.png)
4: DynamoDB table `LegalArticles`.
![alt text](../../images/clean_up_5.png)
5: IAM role created for the Lambda function.
![alt text](../../images/clean_up_6.png)
6: Revoke the Groq API key via the Groq console.
![alt text](../../images/clean_up_7.png)