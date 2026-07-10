---
title: "Week 6 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.6. </b> "
---
### Week 6 Objectives:

* Focus on in-depth research into automated security tools to optimize monitoring capabilities and response to potential risks.
* Strengthen skills in configuring granular permissions in IAM, including distinguishing between roles and users to apply the principle of least privilege in cloud environments.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Study AWS security fundamentals:<br>&nbsp;&nbsp;+ Shared Responsibility Model<br>&nbsp;&nbsp;+ Importance of data protection in the cloud | 05/24/2026 | 05/25/2026 | [AWS: Shared Responsibility Model](https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/shared-responsibility.html) |
| 3   | - Research compliance governance on AWS:<br>&nbsp;&nbsp;+ International regulatory standards<br>&nbsp;&nbsp;+ 5 core functions: Identify, Protect, Detect, Respond, Recover | 05/25/2026 | 05/27/2026 | [AWS: Cloud Compliance Program](https://aws.amazon.com/vi/compliance/) |
| 4   | - Evaluate automated security tools:<br>&nbsp;&nbsp;+ Security Hub<br>&nbsp;&nbsp;+ Trusted Advisor<br>&nbsp;&nbsp;+ Amazon GuardDuty | 05/27/2026 | 05/28/2026 | [AWS: Intelligent Threat Detection – Amazon GuardDuty](https://aws.amazon.com/vi/guardduty/) |
| 5   | - Identity and Access Management (IAM):<br>&nbsp;&nbsp;+ Principle of least privilege<br>&nbsp;&nbsp;+ Root account security and MFA<br>&nbsp;&nbsp;+ Secrets management with Secrets Manager | 05/28/2026 | 05/29/2026 | [AWS: Identity and Access Management (IAM)](https://docs.amazonaws.cn/iam/) |
| 6   | - Deep dive into IAM:<br>&nbsp;&nbsp;+ Distinguish IAM User and IAM Role<br>&nbsp;&nbsp;+ Configure access policies (Policy)<br>&nbsp;&nbsp;+ Attach permissions to EC2/Lambda resources | 05/29/2026 | 05/31/2026 | [AWS Builder Documentation](https://builder.aws.com/content/3C3mJwaTB5NWzcBfEugE7AUx59H/iam-identity-and-access-management) |

### Week 6 Achievements:

* Mastered the AWS Shared Responsibility Model:
  * AWS is responsible for securing physical infrastructure, hypervisors and platform services
  * Customers are responsible for securing data, applications, OS configuration and access control

* Understood the compliance governance framework and 5 core functions:
  * Identify – recognize assets and risks
  * Protect – implement security controls
  * Detect – continuously monitor for anomalies
  * Respond – handle incidents promptly
  * Recover – restore systems after incidents

* Proficiently evaluated and used automated security tools:
  * Security Hub – consolidates and prioritizes security findings from multiple services
  * Trusted Advisor – checks configuration against best practices (security, cost, performance)
  * GuardDuty – intelligent threat detection using ML, analyzing CloudTrail, VPC Flow Logs and DNS logs

* Configured IAM correctly following the principle of least privilege:
  * Root account security: enabled MFA, avoided using root for daily tasks
  * Created IAM Users with limited permissions scoped to specific functions
  * Managed secrets using AWS Secrets Manager and Parameter Store

* Clearly distinguished IAM User vs IAM Role and configured granular access policies:
  * IAM User – fixed identity for people or applications
  * IAM Role – temporary identity attached to EC2/Lambda/AWS services to access resources
  * Inline Policy vs Managed Policy – scope of application and reusability
