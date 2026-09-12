# Project 2: Incident Auto-Assignment System

## Overview
An incident management automation system that eliminates manual triage by routing incidents based on category, priority, and VIP status.

## What Was Built
- **Assignment Rules:** Category-based routing for Hardware, Software, and Network support groups, plus an Order 100 override rule for VIP callers.
- **Business Rules:**
  - `Set Priority 1 for VIP Caller` (Before Insert): Forces Impact=1 and Urgency=1 when Caller.VIP is true.
  - `Log Work Note on P1 Incident` (After Insert/Update): Logs triage work notes automatically via GlideRecord.
- **Client Script:** `onChange` script on Category displaying real-time field messages guiding the user on routing.
- **SLA Definitions:** Configured 15-minute P1 Response, 4-hour P1 Resolution, and 8-hour P2 Resolution SLA targets with automatic attachment and pause logic.

## Structure
- `/screenshots/`: Screenshots of assignment rules, business rules, client scripts, and SLA timers.
- `/update-sets/`: Exported Update Set XML.
