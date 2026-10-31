# ServiceNow Portfolio

Practical administration and automation projects built in a **ServiceNow Personal Developer Instance (PDI)**. This portfolio demonstrates request fulfilment, incident management, access control and data import workflows.

**Start with [Employee Onboarding](./project-1-employee-onboarding/)** for an end-to-end request workflow, or [Incident Automation](./project-2-incident-automation/) for service desk routing and SLA configuration.

## Projects and evidence

| Project | Focus | Included evidence |
| --- | --- | --- |
| [Employee Onboarding](./project-1-employee-onboarding/) | Catalog variables, UI Policies, Client Scripts, manager approval and HR/IT tasks | Screenshots, technical notes, test checklist and XML update sets |
| [Incident Automation](./project-2-incident-automation/) | Category/VIP assignment rules, Business Rules, form messages and P1/P2 SLAs | Screenshots, technical notes, test checklist and XML update set |
| [Leave Management](./project-3-leave-management/) | Scoped application, custom tables, ACLs and data policies | Screenshots and technical notes |
| [IT Asset Requests & Data Import](./project-4-it-asset-portal/) | Record Producers, Order Guides, Import Sets, Transform Maps and Coalesce | Screenshots and technical notes |

## Explore the implementation

Each project README explains its scenario, components and workflow. Screenshot sections link to the available implementation evidence.

- **Request fulfilment:** intake → approval → fulfilment tasks.
- **Incident handling:** routing rules, priority logic and SLA tracking.
- **Access control:** roles, record-level ACL conditions and scoped tables.
- **Data management:** staged imports, field mapping and matching existing records with Coalesce.

## Using the update sets

XML exports are available for the onboarding and incident projects. Review them in a separate development instance: import the XML into Retrieved Update Sets, preview it, inspect conflicts and dependencies, and commit only after resolving preview issues. Instance-specific users, groups, roles and other referenced records may need separate setup.

Leave Management and IT Asset Requests currently provide documentation and screenshots; update-set exports are not included for those projects.

## Scope

These are personal learning projects, not production deployments. The incident project's VIP priority override is a demonstration rule; operational priority should follow the organisation's impact and urgency policy. Test checklists describe validation scenarios and should be rerun in the target instance.

[Profile](https://github.com/Sravan-Gurrala)
