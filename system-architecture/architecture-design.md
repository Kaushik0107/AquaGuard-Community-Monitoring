## Architecture Type:

3-Tier Web Architecture
	•	Presentation Layer (Frontend)
	•	Application Layer (Backend)
	•	Data Layer (Database)

⸻

##  High-Level Architecture

  [ User (Browser / Mobile) ]
            ↓
      Frontend (React / HTML CSS JS)
            ↓
      Backend API (Node.js + Express)
            ↓
        Database (MongoDB)
            ↓
   File Storage (Google Cloud / Local Storage)


  ## Dashboard Module 

Features:
	•	Total Reports
	•	Active Issues
	•	Safe Locations
	•	Map View
	•	Quality Heatmap
	•	Location List

Backend APIs:
GET /api/dashboard/stats
GET /api/reports
GET /api/issues/active

## Report Issue Module 

Two types:
	•	Water Quality Test
	•	Infrastructure Issue

Backend APIs:
POST /api/reports
POST /api/issues

## Issue Tracking Module 

Pipeline shown in design:
User Report → Moderator Review → Validation → Authority Notified → Resolution

Backend APIs:
GET /api/issues
PUT /api/issues/:id/status

Status Enum:
Pending
Under Review
Validated
Authority Notified
Resolved
Rejected

## Community Forum 

Features:
	•	Create Post
	•	Comments
	•	Likes
	•	Categories (Education, Discussion, Tips)

APIs:
POST /api/posts
GET /api/posts
POST /api/comments

## Moderator Panel 

Features:
	•	Login
	•	Review Reports
	•	Validate / Reject
	•	Auto-notify authority (critical issues)

APIs:
POST /api/auth/login
GET /api/moderator/pending
PUT /api/moderator/validate/:id
PUT /api/moderator/reject/:id
