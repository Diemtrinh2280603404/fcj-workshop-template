---
title: "Week 8 Worklog"
date: 2024-01-01
weight: 1
chapter: false
pre: " <b> 1.8. </b> "
---
### Week 8 Objectives:

* Understand the core concepts of Infrastructure as Code (IaC).
* Learn the fundamental principles of AWS CDK and Terraform.
* Get started with foundational knowledge of NodeJS.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Continue exam revision<br>- Explore the core concepts of IaC:<br>&nbsp;&nbsp;+ Benefits over manual configuration<br>&nbsp;&nbsp;+ Declarative vs Imperative approach | 06/07/2026 | 06/08/2026 | [What is Infrastructure as Code?](https://aws.amazon.com/what-is/infrastructure-as-code/) |
| 3   | - Approach AWS CDK:<br>&nbsp;&nbsp;+ Structure: App → Stack → Construct (L1, L2, L3)<br>&nbsp;&nbsp;+ Supported languages: TypeScript, Python, Java, C#<br>&nbsp;&nbsp;+ Synthesize CDK app into CloudFormation template | 06/08/2026 | 06/09/2026 | [AWS CDK Documentation](https://docs.aws.amazon.com/cdk/v2/guide/home.html) |
| 4   | - Study Terraform:<br>&nbsp;&nbsp;+ File structure: main.tf, variables.tf, outputs.tf<br>&nbsp;&nbsp;+ Workflow: init → plan → apply → destroy<br>&nbsp;&nbsp;+ Compare Terraform vs AWS CDK | 06/09/2026 | 06/10/2026 | [Terraform Documentation](https://developer.hashicorp.com/terraform/docs) |
| 5   | - Introduction to NodeJS:<br>&nbsp;&nbsp;+ Install Node.js and npm<br>&nbsp;&nbsp;+ Event Loop and non-blocking I/O model<br>&nbsp;&nbsp;+ Core modules: fs, path, http, events | 06/10/2026 | 06/12/2026 | [Node.js Documentation](https://nodejs.org/docs/latest/api/) |
| 6   | - Hands-on practice combining IaC and NodeJS:<br>&nbsp;&nbsp;+ Deploy AWS infrastructure (S3, Lambda) using CDK or Terraform<br>&nbsp;&nbsp;+ Write Lambda function in NodeJS to handle S3 events | 06/12/2026 | 06/14/2026 | [AWS Getting Started Resource Center](https://aws.amazon.com/getting-started/) |

### Week 8 Achievements:

* Mastered the core concepts of Infrastructure as Code (IaC):
  * Advantages over manual configuration: reusability, version control, environment consistency
  * Two main approaches: Declarative (Terraform) and Imperative (AWS CDK)
  * IaC lifecycle: write → test → deploy → update → destroy

* Understood the foundational structure and architecture model of AWS CDK:
  * App → Stack → Construct hierarchy (L1, L2, L3 constructs)
  * Multi-language support: TypeScript, Python, Java, C#
  * Synthesizing CDK apps into CloudFormation templates

* Clearly understood Terraform syntax and workflow:
  * File structure: `main.tf`, `variables.tf`, `outputs.tf`, `providers.tf`
  * Workflow: `terraform init` → `plan` → `apply` → `destroy`
  * Comparison with CDK: Terraform uses HCL (dedicated language), CDK uses familiar programming languages

* Successfully installed and got acquainted with the NodeJS environment:
  * Installed Node.js and npm, managed packages with `package.json`
  * Understood the Event Loop and Node.js non-blocking I/O model
  * Used core modules: `fs`, `path`, `http`, `events`

* Completed hands-on practice combining IaC and NodeJS:
  * Successfully deployed AWS infrastructure (S3 bucket, Lambda function) using CDK or Terraform
  * Wrote a Lambda function in NodeJS to handle events from S3
