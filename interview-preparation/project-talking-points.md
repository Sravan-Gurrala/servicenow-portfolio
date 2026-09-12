# ServiceNow Projects Interview Guide

## Project 1: Employee Onboarding Application
- **Elevator Pitch:** Designed and implemented an automated employee onboarding solution in ServiceNow to replace manual email coordination between HR and IT support teams.
- **Key Technical Highlights:**
  - Designed a Service Catalog intake form with dynamic variables and a reusable Single-Row Variable Set for personal details.
  - Implemented Catalog UI Policies for conditional field visibility (Needs Laptop Yes/No logic).
  - Authored an onChange Catalog Client Script utilizing g_form.getReference for asynchronous Reporting Manager lookups.
  - Built a Flow Designer workflow orchestrating manager approvals, rejection paths, and parallel task generation for HR Setup, IT Accounts, and Hardware Provisioning.
  - Configured automated email notifications for request confirmations and task assignments.
- **Key Challenge:** Resolving Flow Designer execution context and ensuring reference variables passed correctly to the Ask For Approval action.

## Project 2: Incident Auto-Assignment System
- **Elevator Pitch:** Built an automated incident routing and SLA tracking engine to eliminate manual helpdesk triage and reduce Mean Time to Resolution (MTTR).
- **Key Technical Highlights:**
  - Configured ordered Assignment Rules (VIP override at Order 100, followed by Hardware, Software, and Network category routing).
  - Authored a Before Insert Business Rule to automatically set Priority 1 (Impact=1, Urgency=1) for VIP callers.
  - Developed an After Insert/Update Business Rule leveraging the GlideRecord API to auto-log triage work notes upon P1 detection.
  - Implemented an onChange Client Script to display dynamic routing guidance messages on the form.
  - Configured SLA Definitions for P1 Response (15 min), P1 Resolution (4 hours), and P2 Resolution (8 hours) with On-Hold pause conditions.
- **Key Challenge:** Controlling Business Rule execution order and avoiding recursive updates when writing to work notes using GlideRecord.

## Project 3: Leave Management Scoped Application
- **Elevator Pitch:** Developed a custom Scoped Application in ServiceNow Studio to handle employee leave entitlement and request lifecycles in an isolated namespace.
- **Key Technical Highlights:**
  - Created 3 custom tables (Leave Type, Leave Balance, and Leave Request extending core Task).
  - Extended core Task table to inherit standard lifecycle fields (number, state, work_notes, priority).
  - Configured Table-level Read ACLs requiring application user roles and dynamic conditions (Opened by is Me) to enforce strict record-level security.
  - Built matching UI Policies (client-side form behavior) and Data Policies (server-side mandatory enforcement across imports and web services).
- **Key Challenge:** Enforcing security at both the table and field level while maintaining proper user experience on forms.

## Project 4: IT Asset Request Portal and Data Management
- **Elevator Pitch:** Created self-service portal request assets and engineered a CSV data import pipeline demonstrating deduplication controls and executive reporting.
- **Key Technical Highlights:**
  - Built a Record Producer mapping end-user inputs directly to Incident target records using script mapping.
  - Created an Order Guide bundling hardware package items into a unified checkout interface.
  - Executed a 4-step Data Import pipeline (Source -> Staging Table -> Transform Map -> Target Table).
  - Configured Coalesce on the Email field in the Transform Map to update existing records and insert new records without creating duplicates.
  - Built an Executive Dashboard featuring Pie, Single Score, and Bar chart reports.
- **Key Challenge:** Verifying Coalesce logic during data imports to guarantee data integrity when updating user records.
