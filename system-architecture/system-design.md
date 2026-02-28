# AquaGuard – System Design Document
## 1. Project Overview
   
### 1.1 Introduction

AquaGuard is a web-based civic monitoring platform designed to improve transparency and accountability in water-stressed regions. The system enables community members to submit structured water quality reports and infrastructure-related issues, including supporting files and geolocation data.

Unlike traditional complaint systems, AquaGuard follows a publish-after-validation model, where all submissions are reviewed by moderators before becoming publicly visible. This ensures credibility while maintaining transparency.

The platform provides:

* Structured report submission (with files & geolocation)

* Moderation workflow

* Public dashboard and heatmap

* Resolution lifecycle tracking

* Forum for community discussion

* Simulated authority module

### 1.2 Objectives

The primary objectives of AquaGuard are:

* To prevent misinformation through structured moderation

* To track issue resolution in a controlled lifecycle

* To maintain an auditable trail of actions

* To demonstrate a scalable civic-tech monitoring architecture

### 1.3 Scope

The system supports:

* Web-based access only

* Manual report submission

* Simulated authority workflow

* File uploads and repost functionality

* Geospatial visualization via map integration

The system does not include:

* IoT sensor integration

* Real-time government database integration

* SMS gateway or external civic APIs

### 1.4 Stakeholders

* Community Members (End Users)

Citizens who submit water quality reports and infrastructure issues, view dashboards, track resolution status, and participate in community discussions.

* Moderators

Responsible for validating submitted reports before publication to ensure data credibility and prevent misinformation.

* System Administrators

Manage user roles, oversee moderation workflows, and maintain system configuration.

* Development Team

Responsible for system implementation, deployment, maintenance, and feature evolution.

## 2. Requirements

### Functional Requirements

The system shall:

* Support user authentication (JWT-based)

* Enforce role-based access (User, Moderator, Authority, Admin)

* Allow report submission with file attachments

* Support reposting of similar issues

* Maintain controlled report lifecycle

* Provide moderation approval/rejection

* Display verified reports on dashboard & heatmap

* Trigger notifications on status updates

* Support forum posts and comments

### Non-Functional Requirements

* 95% API response < 300ms

* Geospatial query optimization

* Secure authentication & input validation

* Stateless backend for scalability

* Modular and maintainable code structure

## 3. System Architecture

AquaGuard follows a Three-Tier Layered Architecture:

* Presentation Layer – React.js

* Application Layer – Node.js + Express

* Data Layer – MongoDB


## 3.Alternatives Considered

### 1. Microservices Architecture

Rejected because:

* Overkill for current scope

* Higher operational complexity

* Requires service orchestration & DevOps overhead

* Internship-scale project

* Chosen instead: Modular monolithic architecture
  
Reason: Simpler deployment, faster iteration, easier debugging.

### 2. Relational Database (PostgreSQL)

Rejected because:

Rigid schema structure

Requires migration management for evolving report types

Chosen instead: MongoDB
Reason:

Flexible document model

Native support for nested contaminant arrays

Built-in geospatial indexing

Faster iteration for variable report fields

### 3. Real Authority Integration

Rejected because:

Requires legal and API access

Out of internship scope

Chosen instead: Simulated authority role
Reason:

Demonstrates workflow feasibility without external dependency

### 4. Module Design

System is divided into the following logical modules:

Authentication Module

Report Management Module

Moderation Module

Dashboard & Heatmap Module

Forum Module

Notification Module

File Handling Module

Each module operates independently but communicates via defined API contracts.

## 5. Database Design

* MongoDB is used for flexible and scalable data storage.

* Core Collections

* Users

* Reports

* ModerationLogs

* Posts

* Comments

* Notifications

Geospatial index is applied on:

latitude

longitude

Status field is indexed for:

Fast moderation filtering

Efficient dashboard queries

ER Diagram Placement

The Entity-Relationship Diagram (ERD) is provided below:

![AquaGuard ER Diagram](./images/er-diagram.png)

Placement Recommendation:
Insert the ER diagram immediately after this Database Design section.

The ERD illustrates:

User → Reports (1:N)

Report → ModerationLogs (1:N)

User → Posts (1:N)

Post → Comments (1:N)

User → Notifications (1:N)

The ER diagram serves as the structural blueprint of the system’s data layer.

6. API Design

The system exposes RESTful APIs.

Design Principles

Stateless communication

JSON request/response

Standard HTTP status codes

Role-based middleware enforcement

API categories:

Authentication APIs

Report APIs

Moderation APIs

Forum APIs

Notification APIs

All protected routes require JWT validation.




