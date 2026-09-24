---
Title: "Week 1 Worklog"
Date: 14-09-2026
Weight: 1
Chapter: false
pre: " 1.1 "
---

### Week 1 Objectives:

* Understand and practice permission management and secure access control on AWS using IAM (User, Group, Policy, Role, Switch Role).
* Understand the Amazon VPC virtual network structure, routing and security components, and how to set up an AWS Site-to-Site VPN connection.
* Master the process of launching, managing, and deploying real-world applications on Amazon EC2 virtual server services (Linux & Windows).
* Learn how to grant applications secure access to AWS services via IAM Roles and utilize the AWS CloudShell environment.

### Tasks to be implemented this week:
| Day | Task                                                                                                                                                                                       | Start Date   | Completion Date | Resource Source                           |
| --- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | --------------- | ----------------------------------------- |
| Mon | - Learn about AWS IAM (User, Group, Policy, Role) <br> - **Hands-on Practice:** <br>&emsp; + Create IAM Group & IAM User <br>&emsp; + Create IAM Role & Operator User <br> &emsp; + Configure & Use Switch Role <br>&emsp; + Clean up resources                                                                                             | 14/09/2026   | 14/09/2026      | <https://000002.awsstudygroup.com>
| Tue | - Learn about Amazon VPC & AWS Site-to-Site VPN (Subnet, Route Table, IGW, NAT Gateway, Security Group, NACL) <br> - **Hands-on Practice:** <br>&emsp; + Create VPC, Subnet, Internet Gateway & Route Table <br>&emsp; + Configure Security Group & VPC Flow Logs <br>&emsp; + Deploy EC2 Instance, NAT Gateway & SSM Session Manager <br>&emsp; + Configure AWS Site-to-Site VPN connection <br>&emsp; + Configure advanced VPN with Strongswan & Transit Gateway (Optional) <br>&emsp; + Resource cleanup                                            | 15/09/2025   | 15/09/2026      | <https://000003.awsstudygroup.com> |
| 4   | - Learn about Amazon EC2 (Elastic Compute Cloud) <br> - **Hands-on:** <br>&emsp; + Prepare VPC & Security Groups for Linux and Windows <br>&emsp; + Launch & Connect to Microsoft Windows Server 2025 Instance <br>&emsp; + Launch & Connect to Amazon Linux Instance <br>&emsp; + Basic EC2 operations (Change Instance Type, manage EBS Snapshots, Custom AMI, recover access) <br>&emsp; + Deploy user management application on Amazon Linux (LAMP Stack / Node.js) <br>&emsp; + Deploy Node.js application on Windows Server (XAMPP / Node.js) <br>&emsp; + Configure IAM for cost management & EC2 resource usage limits <br>&emsp; + Resource cleanup | 16/09/2026   | 16/09/2026      | <https://000004.awsstudygroup.com> |
| 5   | - Learn about granting applications access to AWS services via IAM Roles <br> - **Hands-on:** <br>&emsp; + Create IAM Role to grant access to AWS services <br>&emsp; + Configure & Assign IAM Role to application (EC2/Lambda) <br>&emsp; + Verify application access to AWS services <br>&emsp; + Resource cleanup                               | 17/09/2026   | 17/09/2026      | <https://000048.awsstudygroup.com> |
| 6   | - Introduction to AWS CloudShell (Command-line environment) <br> - **Hands-on practice:** <br>&emsp; + Initialize AWS CloudShell environment <br>&emsp; + Basic Linux commands & file operations <br>&emsp; + Resource management using AWS CLI on CloudShell <br>&emsp; + Upload/Download files between CloudShell and local machine <br>&emsp; + Resource cleanup                                                                                         | 18/09/2026   | 18/09/2026      | <https://000049.awsstudygroup.com> |


### Week 1 Achievements:

* Understood and practiced access management with AWS IAM:
  * Understood and practiced access management with AWS IAM:
  * Configured IAM Roles & Operator Users. 
  * Practiced "Switch Role" for secure role transitions.

* Mastered Amazon VPC network creation and configuration:
  * Created VPC, Subnets, Internet Gateway, and Route Tables. 
  * Established security with Security Groups and monitoring with VPC Flow Logs. 
  * Deployed NAT Gateway, SSM Session Manager, and AWS Site-to-Site VPN connections. 
  * Configured advanced VPN setups using Strongswan & Transit Gateway.

* Mastered the administration and usage of Amazon EC2 virtual servers:
  * Successfully launched, configured, and connected to Microsoft Windows Server 2025 & Amazon Linux instances. 
  * Performed EC2 administrative tasks: changing instance types, managing EBS snapshots and custom AMIs, and recovering access. 
  * Deployed user management applications (Node.js/LAMP Stack) on both Linux and Windows environments. * Apply IAM policies to control costs and limit EC2 resource usage.

* Grant permissions for applications and operations on AWS CloudShell:
  * Create and assign an IAM role for applications (EC2/Lambda) to securely access AWS services. 
  * Demonstrate proficiency in the AWS CloudShell CLI environment (executing Linux commands, managing resources via AWS CLI, and uploading/downloading files).

* Perform resource cleanup after each practical exercise to optimize costs.