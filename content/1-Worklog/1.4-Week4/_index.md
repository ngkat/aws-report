---
title: "Week 4 Worklog"
date: 05-10-2026
weight: 1
chapter: false
pre: "  1.4  "
---


### Week 4 Objectives:

* Understand and practice building automated Extract, Transform, and Load (ETL) pipelines using AWS Glue.
* Master querying and analyzing unstructured and semi-structured data stored in S3 using SQL with Amazon Athena.
* Become proficient in multi-service workflow orchestration using AWS Step Functions.
* Understand cloud data warehouse architecture and high-performance data loading/querying techniques with Amazon Redshift.
* Master the setup and management of big data processing clusters (frameworks such as Apache Spark, Hadoop, and Hive) on Amazon EMR.

### Tasks to be implemented this week:
| Day | Task                                                                                                                                                                                       | Start Date   | Completion Date | Resources                                 |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| Mon | - Explore AWS Glue (Serverless Data Integration Service) <br> - **Hands-on Practice:** <br>&emsp; + Initialize AWS Glue Data Catalog & configure Glue Crawler for automatic schema discovery <br>&emsp; + Create and configure AWS Glue Databases & Tables <br>&emsp; + Build and launch ETL (Extract, Transform, Load) tasks using AWS Glue Jobs <br>&emsp; + Perform data transformation and save results to S3 / Redshift / DynamoDB <br>&emsp; + Automate and schedule ETL Jobs using AWS Glue Triggers / Workflows <br>&emsp; + Resource cleanup                                                                                             | 05/10/2026   | 05/10/2026      | <https://000092.awsstudygroup.com>
| 3   | - Introduction to Amazon Athena (Interactive Query Service) - **Hands-on:** <br>&emsp; + Configure the query result location on S3 <br>&emsp; + Create a database and tables in Athena based on data stored in Amazon S3 <br>&emsp; + Execute SQL queries to analyze and explore data directly on S3 <br>&emsp; + Configure partitioning and optimized data formats (Parquet/ORC) to improve performance and reduce query costs <br>&emsp; + Integrate Athena with AWS Glue Data Catalog for automated schema management <br>&emsp; + Resource cleanup                                            | 06/10/2026   | 06/10/2026      | <https://000094.awsstudygroup.com> |
| 4   | - Introduction to AWS Step Functions (Serverless Visual Workflow) <br> - **Hands-on:** <br>&emsp; + Create a State Machine in AWS Step Functions using Visual Workflow Studio or Amazon States Language (ASL) <br>&emsp; + Configure basic states (Task, Choice, Parallel, Map, Pass, Fail) <br>&emsp; + Integrate Step Functions with other AWS services (AWS Lambda, Amazon SQS, Amazon SNS, DynamoDB) <br>&emsp; + Execute the State Machine, handle input/output processing, and monitor the control flow <br>&emsp; + Configure Error Handling (Retry & Catch) to manage exceptions in the workflow <br>&emsp; + Resource cleanup | 07/10/2026   | 07/10/2026      | <https://000130.awsstudygroup.com> |
| 5   | - Learn about Amazon Redshift (Cloud Data Warehouse) <br> - **Hands-on practice:** <br>&emsp; + Provision Amazon Redshift Cluster / Redshift Serverless <br>&emsp; + Configure VPC networking, Security Groups, and IAM Roles for S3 data connectivity <br>&emsp; + Create Database, Schema, and Tables optimized with Distribution Keys & Sort Keys <br>&emsp; + Load data from Amazon S3 into Redshift using the COPY command <br>&emsp; + Execute high-performance SQL queries for data analysis <br>&emsp; + Resource cleanup                  | 08/10/2026   | 08/10/2026      | <https://000093.awsstudygroup.com> |
| 6   | - Learn about Amazon EMR (Elastic MapReduce - Managed Big Data Framework) <br> - **Hands-on practice:** <br>&emsp; + Provision an EMR Cluster with big data processing frameworks (Apache Spark / Hadoop / Hive) <br>&emsp; + Configure IAM Roles, EC2 Instance Types, and Subnets for the Cluster <br>&emsp; + Prepare and upload data/processing scripts (Spark / PySpark jobs) to Amazon S3 <br>&emsp; + Submit data processing tasks (Steps / Jobs) to the EMR Cluster <br>&emsp; + Monitor execution, store output results in S3, and manage the EMR cluster lifecycle <br>&emsp; + Clean up resources                                                                                         | 09/10/2026   | 09/10/2026      | <https://000095.awsstudygroup.com> |


### Week 4 Achievements:

* Built an automated data integration and transformation pipeline using AWS Glue:
  * Initialized a Glue Crawler to automatically Schema scanning and discovery, storing metadata in the AWS Glue Data Catalog.
  * Setting up AWS Glue databases and tables, and creating ETL scripts to transform and store data in S3, Redshift, or DynamoDB.
  * Automating and scheduling ETL jobs using Glue Triggers and Workflows.

* Performing ad-hoc data queries on S3 with Amazon Athena:
  * Creating Athena databases and tables that connect directly to data on Amazon S3.
  * Executing SQL queries for direct data analysis without provisioning server infrastructure.
  * Optimizing costs and query performance through partitioning and converting data to columnar formats (Parquet/ORC).

* Orchestrating complex workflows with AWS Step Functions:
  * Designing visual State Machines using Visual Studio or Amazon States Language (ASL).
  * Successfully integrating Step Functions to orchestrate multiple services (Lambda, SQS, SNS, DynamoDB).
  * Configuring error handling, retry mechanisms (Retry & Catch), and data flow control across steps.

* Deploying large-scale analytical data warehouses with Amazon Redshift:
  * Provisioning Redshift Clusters or Serverless instances with secure VPC connectivity.
  * Configuring Distribution Keys and Sort Keys to optimize queries on large datasets.
  * Using the COPY command for high-speed data ingestion from Amazon S3 into Redshift.

* Processing big data using frameworks with Amazon EMR:
  * Deploying EMR clusters configured with Spark, Hadoop, and Hive.
  * Submitting and managing data processing tasks (Spark/PySpark jobs) based on scripts stored in S3.
  * Saving analysis results to S3 and optimizing costs by terminating the cluster after job completion.
  
* Optimize costs by cleaning up resources after each practice session.