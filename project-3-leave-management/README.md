# Project 3: Leave Management Scoped Application

## Overview
A custom scoped application built in ServiceNow Studio to manage employee leave requests outside the global scope.

## What Was Built
- **Scoped App Structure:** Created in Studio with unique scope namespace `x_leave_mgmt`.
- **Custom Tables:**
  - `Leave Type`: Standalone table for leave categories and annual quotas.
  - `Leave Balance`: Standalone table tracking entitlement per employee.
  - `Leave Request`: Custom table extending core `Task` table to inherit lifecycle fields.
- **ACL Security:** Table-level Read ACL enforcing dynamic `Opened by is (dynamic) Me` record-level access for application users.
- **Policies:**
  - **UI Policy:** Makes `Handover Person` visible and mandatory when leave duration > 3 days (client-side).
  - **Data Policy:** Enforces `Reason` as mandatory across form UI, imports, and web services (server-side).

## Structure
- `/screenshots/`: Screenshots of Studio app layout, custom tables, ACLs, policies, and live form.
