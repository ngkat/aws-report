---
title : "Phase 2 – Backend: from database to Lambda and API"
date : 15-10-2026
weight : 4
chapter : false
pre : "  5.4  "
---

#### Overview

| Item         | Content                                                                                     |
| ------------ | ------------------------------------------------------------------------------------------- |
| Purpose      | A serverless backend that retrieves legal articles, calls the LLM and exposes a stable API. |
| AWS services | DynamoDB, Lambda, API Gateway, CloudWatch.                                                  |
| Input        | HTTP POST with the user's question.                                                         |
| Output       | Standard JSON with the answer or an error code.                                             |
| Depends on   | Phase 1 prompt; Groq API key.                                                               |

#### 5.4.1. Build the knowledge base on DynamoDB

**Goal** <br>
Store legal articles in a table that Lambda can query. <br>
**Steps** <br>
1. Create the table LegalArticles .
2. Design the item structure (for example article number, title, content, keywords).
3. Load the articles extracted from Decree 13/2023/ND-CP, including provisions on using ID card data, personal data and violation handling.
4. Check the item count against the source document.

Limitation: lookup is keyword-based, so a question using different wording may miss the right article.

**Verify** <br>
The table returns the expected articles when scanned in the console.

####