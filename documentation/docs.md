# AquaGuard – Community Water Monitoring System

## SDG Goal 6: Clean Water & Sanitation

AquaGuard is a full-stack MERN web application designed to improve transparency and efficiency in water quality issue reporting through community participation.

---

# ABSTRACT

## Problem Statement

Water quality monitoring in many communities depends on manual reporting systems. Citizens must visit offices or make phone calls to register complaints. This process is slow, lacks transparency, and does not provide proper tracking mechanisms. Communication gaps between citizens and authorities lead to delayed responses and unresolved issues.

## Solution – AquaGuard System

AquaGuard is a community-driven web platform that enables users to:

- Submit water-related complaints
- Add location details using maps
- Upload supporting evidence (images/files)
- Track complaint status in real-time

Moderators and authorities can review, validate, and manage reports using a centralized dashboard.

## Technologies Used

- React.js (Frontend)
- Node.js & Express.js (Backend)
- MongoDB (Database)
- Google Maps API (Location Tracking)
- JWT (Authentication)
- Cloud Storage (File Upload)

## Outcome

The system:
- Improves transparency
- Enables real-time complaint tracking
- Reduces response time
- Strengthens communication between citizens and authorities

---

# CHAPTER 1: INTRODUCTION

## 1.1 Background

Water quality monitoring ensures safe drinking water and environmental protection. Traditional systems rely on manual inspections and citizen complaints, which suffer from:

- Delayed complaint registration
- Lack of digital records
- No real-time tracking
- Poor transparency
- Inefficient communication

There is a need for a digital platform for quick reporting and monitoring.

## 1.2 Problem Statement

The existing manual complaint system is inefficient and lacks transparency. Citizens face difficulties reporting issues, and authorities cannot easily verify or track complaints. This reduces public trust and delays action.

## 1.3 Objectives

- Enable community-based reporting
- Provide real-time monitoring dashboard
- Validate reports via moderators
- Notify users and authorities about status updates

## 1.4 Scope of the Project

- Web-based complaint system
- Role-based access (Users & Moderators)
- Location tracking using maps
- Secure authentication
- Evidence upload support
- Real-time status updates

---

# CHAPTER 2: LITERATURE SURVEY

## Existing Water Monitoring Systems

- Focus mainly on IoT and lab testing
- Limited community participation
- Lack centralized dashboards

## Government Reporting Applications

- Not always user-friendly
- Limited tracking
- Minimal data visualization

## Improvement by AquaGuard

- Community reporting
- Map-based visualization
- Dashboard analytics
- Automated notifications

---

# CHAPTER 3: SYSTEM ANALYSIS

## 3.1 Existing System

- Manual complaint submission
- Phone calls or physical visits
- Paper-based records
- No real-time tracking
- Lack of transparency

## 3.2 Proposed System

AquaGuard:

- Online complaint submission
- Centralized database storage
- Map-based issue display
- Moderator validation
- Automated notifications

## 3.3 Feasibility Study

### Technical Feasibility

Uses stable and scalable technologies:
- React.js
- Node.js
- MongoDB

### Economic Feasibility

- Open-source stack
- Minimal cloud hosting costs

### Operational Feasibility

- User-friendly interface
- Minimal training required

---

# CHAPTER 4: SYSTEM DESIGN

## 4.1 System Architecture

Architecture Overview:

Users / Moderators  
↓  
React Frontend  
↓  
Node.js + Express Backend (REST API)  
↓  
MongoDB Database  
↓  
Cloud Storage & Email Notification Service  

## 4.2 Data Flow Diagram

### Level 0

Users → AquaGuard System → Moderators → Authorities

### Level 1

Submission Phase:
- User submits report
- Data stored in database (Pending)

Moderation Phase:
- Moderator reviews report
- Approve / Reject

Approval Branch:
- Status updated
- Heatmap updated
- Public interface updated

Notification Branch:
- Authorities notified

## 4.3 Database Design

### Users Collection

- id
- name
- email
- password
- role (user/moderator)
- created_at

### Reports Collection

- id
- user_id
- location_name
- latitude
- longitude
- quality_level
- contaminants
- lab_report_file
- status (Pending / Validated)
- created_at

### Issues Collection

- id
- user_id
- issue_type
- severity
- photos
- status
- created_at

### Notifications Collection

- id
- user_id
- type (Report / Issue / Comment)
- is_read
- created_at

---

# CHAPTER 5: IMPLEMENTATION

## 5.1 Frontend (React.js)

Components:

- Login Component
- Registration Component
- Dashboard Component
- Report Submission Form
- Moderator Panel
- Map Component

## 5.2 Backend (Node.js + Express)

REST APIs:

- POST /register
- POST /login
- POST /submit-report
- GET /get-reports
- PUT /update-status

JWT is used for authentication.

## 5.3 Database Implementation

MongoDB with Mongoose schemas for:

- Users
- Reports
- Notifications

---

# CHAPTER 6: RESULTS AND OUTPUT

The system successfully provides:

- User Dashboard
- Login Page
- Moderator Panel
- Issue Tracking Page

Features:

- Real-time complaint tracking
- Moderator validation workflow
- Map visualization
- Notification system

---

# CHAPTER 7: CONCLUSION

AquaGuard has been successfully implemented as a full-stack MERN application. It provides a transparent and efficient system for reporting water quality issues.

The project digitalizes complaint management and strengthens communication between communities and authorities.

---

# CHAPTER 8: FUTURE ENHANCEMENTS

- AI-based contamination prediction
- IoT sensor integration
- SMS alert system
- Mobile application version
- Advanced analytics dashboard

---

# AUTHOR

Project Developed By: ANSBID  
Technology Stack: MERN  
Year: 2026
