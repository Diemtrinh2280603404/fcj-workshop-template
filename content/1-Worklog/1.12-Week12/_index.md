---
title: "Week 12 Worklog"
date: 2024-01-01
weight: 2
chapter: false
pre: " <b> 1.12. </b> "
---
### Week 12 Objectives:

* Complete community interaction features for the FlashLearn system.
* Build scoring logic and user ranking system.
* Deploy a hierarchical comment system.
* Track user activity into the database.
* Finalize technical documentation and project handover.

### Tasks to be carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | ---- | ---------- | --------------- | ------------------ |
| 2   | - Team meeting to design community interaction APIs:<br>&nbsp;&nbsp;+ Flashcard voting API (upvote/downvote)<br>&nbsp;&nbsp;+ Quiz ranking API based on time and correct answer ratio | 07/05/2026 | 07/06/2026 | |
| 3   | - Implement scoring logic and ranking system:<br>&nbsp;&nbsp;+ Add points: upvote, Quiz completion, approved Flashcard<br>&nbsp;&nbsp;+ Deduct points: downvote, community guideline violations<br>&nbsp;&nbsp;+ Leaderboard categorized by week/month/all-time | 07/06/2026 | 07/07/2026 | |
| 4   | - Design hierarchical comment system:<br>&nbsp;&nbsp;+ Data structure supporting nested replies (parent_id)<br>&nbsp;&nbsp;+ Automatically update comment_count counter<br>&nbsp;&nbsp;+ Moderate comment content via Lambda | 07/07/2026 | 07/08/2026 | |
| 5   | - Complete additional features:<br>&nbsp;&nbsp;+ "Favorite" feature for Flashcard/Quiz<br>&nbsp;&nbsp;+ Track user activity in user_activities table<br>&nbsp;&nbsp;+ Activity data feeds smart learning recommendation engine | 07/08/2026 | 07/09/2026 | |
| 6   | - Team meeting: Finalize documentation and project handover:<br>&nbsp;&nbsp;+ Complete API documentation with Swagger/OpenAPI spec<br>&nbsp;&nbsp;+ Full system ERD (10+ tables)<br>&nbsp;&nbsp;+ Handover package: architecture, deployment guide, accounts | 07/09/2026 | 07/10/2026 | |

### Week 12 Achievements:

* Completed community interaction APIs for FlashLearn:
  * Flashcard voting API: POST /flashcards/{id}/vote (upvote/downvote)
  * Quiz ranking API: score calculated based on completion time and correct answer ratio
  * Leaderboard updated in real time via DynamoDB

* Successfully deployed scoring logic and user ranking system:
  * Points awarded for upvotes, Quiz completions and approved Flashcard submissions
  * Points deducted for downvotes or community guideline violations
  * Leaderboard categorized by week/month/all-time

* Built a complete hierarchical comment system:
  * Data structure supports nested comments and replies (parent_id)
  * Automatically updates comment_count on each Flashcard/Quiz
  * Comment content moderated via Lambda before being displayed

* Completed the Favorite feature and user activity tracking:
  * Users can save favorite Flashcards/Quizzes to their personal collection
  * The `user_activities` table records all user actions: views, study sessions, votes, comments
  * Activity data feeds the smart learning recommendation engine

* Successfully finalized technical documentation and project handover:
  * Complete API documentation with Swagger/OpenAPI spec for all endpoints
  * Comprehensive system ERD covering 10+ tables and their relationships
  * Handover package includes: system architecture, deployment guide, accounts and access credentials
