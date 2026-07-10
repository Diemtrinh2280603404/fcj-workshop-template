---
title: "Week 11 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.11. </b> "
---
### Week 11 Objectives:

* Design core APIs for the FlashLearn system.
* Build the database and content management admin interface.
* Deploy an automated content approval workflow.
* Optimize storage resource management with S3 Presigned URLs.
* Finalize technical documentation and the Entity Relationship Diagram (ERD).

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Design RESTful APIs for Flashcard and Quiz:<br>&nbsp;&nbsp;+ POST /flashcards (Create), GET, PUT, DELETE<br>&nbsp;&nbsp;+ Validate input data (character limits, question format)<br>&nbsp;&nbsp;+ Integrate JWT token via API Gateway Authorizer | 06/28/2026 | 06/29/2026 | [Build RESTful APIs with API Gateway](https://docs.aws.amazon.com/apigateway/latest/developerguide/getting-started.html) |
| 3   | - Build database and admin interface:<br>&nbsp;&nbsp;+ Create flashcards table with status column (pending/approved/rejected)<br>&nbsp;&nbsp;+ Create quiz_results table<br>&nbsp;&nbsp;+ Admin interface to view, approve and reject content | 06/29/2026 | 06/30/2026 | |
| 4   | - Deploy automated content approval workflow:<br>&nbsp;&nbsp;+ When admin approves → Lambda updates search index<br>&nbsp;&nbsp;+ EventBridge notifies content creators on status change<br>&nbsp;&nbsp;+ Save approval history to audit_logs table | 07/01/2026 | 07/02/2026 | |
| 5   | - Create S3 Presigned URLs for upload/download:<br>&nbsp;&nbsp;+ Time-limited Presigned URL for direct S3 upload<br>&nbsp;&nbsp;+ CloudFront distributes images/audio with signed URLs<br>&nbsp;&nbsp;+ Reduce server bandwidth load | 07/02/2026 | 07/03/2026 | [CloudJourney AWS Study Group](https://cloudjourney.awsstudygroup.com/) |
| 6   | - Finalize technical documentation and ERD:<br>&nbsp;&nbsp;+ Full ERD: Users, Flashcards, Decks, Quiz, QuizResults, Battle, Progress, AuditLogs<br>&nbsp;&nbsp;+ API documentation with endpoint, request/response schema and error codes | 07/03/2026 | 07/05/2026 | [Entity Relationship Diagram Tutorial](https://lucid.co/diagram/erd/tutorial) |

### Week 11 Achievements:

* Designed and finalized the core RESTful APIs for the FlashLearn system:
  * Flashcard API: POST /flashcards (Create), GET /flashcards/{id}, PUT, DELETE with input validation
  * Quiz API: structured question format, answer format and character limits
  * Integrated JWT token authentication via API Gateway Authorizer

* Successfully built the database and content management admin interface:
  * Created `flashcards` table with `status` column (pending/approved/rejected) and `quiz_results` table
  * Admin interface allows viewing, approving, rejecting and editing flashcard content
  * Admin permissions managed via a dedicated IAM Role

* Deployed an automated content approval workflow:
  * When admin approves content → Lambda automatically triggers to update the search index
  * EventBridge sends notifications to content creators when status changes
  * Approval history saved to the `audit_logs` table

* Optimized storage resource management with S3 Presigned URLs:
  * Generated time-limited Presigned URLs allowing users to upload directly to S3 (bypassing the server)
  * CloudFront distributes images/audio from S3 with signed URLs, protecting resources from unauthorized access
  * Reduced server bandwidth load and improved upload speed

* Completed technical documentation and system ERD:
  * Full ERD including entities: Users, Flashcards, Decks, Quiz, QuizResults, Battle, Progress, AuditLogs
  * Defined 1-N and N-N relationships, primary keys and foreign keys for each table
  * Complete API documentation with endpoint descriptions, request/response schemas and error codes
