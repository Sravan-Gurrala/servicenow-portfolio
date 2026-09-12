# Project 1: Employee Onboarding Application

## Overview
A Service Catalog request application designed to streamline new hire onboarding across HR and IT departments.

## What Was Built
- **Service Catalog Intake:** Category `Employee Onboarding` and Catalog Item `New Employee Onboarding Request`.
- **Variables & Variable Sets:** Single-row Variable Set for personal details plus custom variables for department, manager, employment type, start date, and hardware needs.
- **Form Behavior:**
  - **Catalog UI Policy:** Dynamically displays and enforces `Laptop Type` when `Needs Laptop` is checked Yes.
  - **Catalog Client Script:** Uses `g_form.getReference()` on the `Reporting Manager` field to display manager details automatically.
- **Flow Designer:** `Employee Onboarding Process` flow triggered on order, retrieving catalog variables, requesting manager approval, handling rejections, and auto-generating fulfillment tasks for HR and IT Support.
- **Notifications:** Configured email alerts for request confirmation and task assignment.

## Structure
- `/screenshots/`: Screenshots of form layout, flow designer, and task execution.
- `/update-sets/`: Exported Update Set XML.
