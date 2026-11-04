---
title : "Final output and next steps"
date : 15-10-2026
weight : 7 
chapter : false
pre : "  5.7  "
---

#### Final output

* A complete serverless backend that scales automatically and, by the team's measurement, costs $0 while staying within the AWS Free Tier.
* A working RAG flow: each request retrieves articles from DynamoDB and combines them with the LLM to give a grounded answer.
* A stable API endpoint, ready for the static website and for team members to test.

#### Known limitations

* Keyword retrieval can miss relevant articles.
* The answer is plain text; there is no structured risk level yet.
* The LLM runs outside AWS and the API has no authentication yet.

#### Next steps

* Structured response with risk level (Low / Medium / High / Insufficient evidence), provisions, evidence and sources.
* Human-confirmed incident report with an Amazon SNS email alert (summary only, no sensitive data).
* Conversation history in DynamoDB with TTL.
* Evaluate Amazon Bedrock and Bedrock Knowledge Bases to keep all data inside AWS (check current pricing and region availability first).