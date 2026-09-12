# High-Yield CSA Technical Questions and Answers

## 1. What is the evaluation order of Access Control Lists (ACLs)?
- **Answer:** Table-level ACLs are evaluated first (`table` or `table.None`). If access is granted, Field-level ACLs (`table.field` or `table.*`) are evaluated second. Both table and field ACLs must pass for a user to access a specific field.

## 2. What is the difference between a UI Policy and a Data Policy?
- **Answer:** A UI Policy runs client-side on the browser form only. A Data Policy runs server-side and enforces mandatory/read-only rules across forms, Excel data imports, REST/SOAP APIs, and background scripts. Data Policies cannot hide fields.

## 3. What is Coalesce in a Transform Map?
- **Answer:** Coalesce designates a field as the unique matching key during data imports. If a record with a matching key exists in the target table, it is updated. If no match is found, a new record is inserted, preventing duplicate records.

## 4. What happens when a custom table extends the core Task table?
- **Answer:** The custom table inherits all fields and relationships from the Task table automatically (such as `number`, `state`, `priority`, `assignment_group`, `assigned_to`, and `work_notes`).

## 5. What is the difference between a Catalog Item and a Record Producer?
- **Answer:** A Catalog Item creates a Requested Item (`sc_req_item`) and triggers fulfillment workflows/tasks. A Record Producer creates a record directly on a target table (such as `incident` or `change_request`) without generating catalog requests.

## 6. How do Assignment Rules evaluate when multiple rules exist?
- **Answer:** Assignment Rules evaluate in ascending order by the `Order` field value. The first rule whose conditions match assigns the record, and evaluation stops immediately.

## 7. What are the 4 timing options for Business Rules?
- **Answer:** `before` (runs before record is saved to database), `after` (runs after record is saved to database), `async` (runs in background transaction after save), and `display` (runs when form is loaded before rendering to user).
