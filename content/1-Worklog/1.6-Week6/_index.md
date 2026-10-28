---
title: "Week 6 Worklog"
date: 19-10-2026
weight: 1
chapter: false
pre: "  1.6  "
---


### Week 6 Objectives:

* Continue working on the group project.

### Tasks to be carried out this week:
| Day | Task                                                                                                                                                                                                   | Start Date | Completion Date | Reference Material                        |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------- | --------------- | ----------------------------------------- |
| 2   | - Set up backend using AWS Console <br>&emsp; + Call the Groq API (using the `qwen/qwen3.8-27b` model)                                                                                                   | 19/10/2026 | 19/10/2026      |
| 3   | - Set up backend using AWS Console <br>&emsp; + Build a RAG pipeline                                              | 20/10/2026 | 20/10/2026      |
| 4   | - Setting up the backend using the AWS Console <br>&emsp; + Building Amazon API Gateway | 21/10/2026 | 21/10/2026      |
| 5   | - Set up Backend with AWS Console <br>&emsp; + Input Validation <br>&emsp; + Standardized Error Handling                            | 22/10/2026 | 22/10/2026      |
| 6   | - Set up the backend using the AWS Console <br>&emsp; + Build the web chat interface (frontend)                                                                                     | 23/10/2026 | 23/10/2026      |


### Week 6 Achievements:

* Configured the secure environment variable (`GROQ_API_KEY`) on AWS Lambda.
* Resolved the "Error 1010 / 403" issue caused by Cloudflare blocking AWS Lambda's IP range.
* Successfully integrated a browser-mimicking header (`User-Agent`) into the Python `urllib` code to bypass firewalls.
* Integrated `boto3` within Lambda to scan and extract legal data, then inject it into the prompt for the Groq API (`qwen/qwen3.8-27b`).
* Configured a `POST /chat` route linked directly to the AWS Lambda function responsible for RAG (Retrieval-Augmented Generation) processing.
* Set up the default stage (`$default`) and retrieved the public Invoke URL.
* Enabled CORS (Access-Control-Allow-Origin: *, Methods: POST, Headers: Content-Type) to allow the frontend to call the API.
* Standardized the HTTP response structure across the entire system, including all necessary CORS headers.
* Implemented error handling for missing `GROQ_API_KEY` environment variables.
* Implemented error handling for network timeouts.
* Built a complete chat interface, utilizing Tailwind CSS for a modern, user-friendly layout.
* Verified that the application runs smoothly at `http://localhost:8000`.
* Obtained the public S3 website URL, tested it in a personal browser, and shared the link with team members to verify access permissions.