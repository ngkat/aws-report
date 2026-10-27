---
title: "Blog 2"
date: 27-10-2026
weight: 1
chapter: false
pre: "  3.2  "
---

# AWS LEARNING CORNER: WHAT SHOULD AWS BEGINNERS KEEP IN MIND TO AVOID A "SHOCKING" END-OF-MONTH BILL?


A common scenario for those just starting out with AWS is accidentally launching a test resource and forgetting to shut it down—only to be met with an unexpected bill at the end of the month. Learning to control costs not only gives you peace of mind while practicing, but it is also a fundamental skill for managing cloud infrastructure.

Below are some key settings and considerations to help you manage your budget effectively from the very beginning.

---

### 1. Setting Up AWS Budgets & Billing Alerts

This is the first step you should take immediately after creating an AWS account.

* **Mechanism:** Configure a safe budget threshold (e.g., $5 or $10). If your actual or forecasted costs exceed this limit, the system will automatically send an email notification.
* **Benefit:** Prevents resources from running in the background indefinitely without being detected in a timely manner.

---

### 2. Making Proper Use of the AWS Free Tier

* **Time Limits:** For instance, EC2 offers 750 hours per month for `t2.micro` or `t3.micro` instances (depending on the region). If you run two such instances simultaneously, the usage time will be doubled, quickly exceeding the free-tier limit.
* **Capacity Limits:** Services like S3 and EBS have specific caps on storage capacity and the number of requests. Be sure to carefully review the service terms before provisioning resources.

---

### 3. Cleaning up unused resources

"Junk" or orphaned resources are often the source of hidden costs:

* **Shut down or delete EC2 instances:** Stop test servers when they are not in use.
* **Watch out for Elastic IPs:** Elastic IPs are only free when associated with an EC2 instance that is in the "Running" state. If an Elastic IP is disassociated or attached to an instance that is in the "Stopped" state, you will still be charged a retention fee.
* **Delete unattached EBS volumes and snapshots:** When an EC2 instance is deleted, certain EBS volumes or automatically created snapshots may remain as orphaned resources, continuing to incur storage costs.

---

### 4. Detailed Monitoring with AWS Cost Explorer

* Visualization Tool: AWS Cost Explorer provides charts to analyze costs over time, by service, or by tag.
* Regular Reviews: Checking your cost reports once or twice a week helps you quickly identify services that are consuming an unusual amount of your budget.

---

### 5. Conclusion

Cost optimization and control are essential components of the mindset required for working with cloud computing. Establishing a secure infrastructure from the outset allows you to explore and experiment with AWS services with peace of mind, without having to worry about costs.

---

![alt text](<../../images/aws cost optimization.png>)

https://www.facebook.com/groups/awsstudygroupfcj/posts/2317495209015438/?notif_id=1793075766463069&notif_t=group_post_approved&ref=notif