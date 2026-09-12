# Employee Onboarding — Technical Notes

## Request Structure

```text
Catalog Item
    ↓
Request [sc_request]
    ↓
Requested Item [sc_req_item]
    ↓
Catalog Tasks [sc_task]
Catalog Variables
Variables collect information from the requester. A variable set groups reusable variables that can be attached to multiple catalog items.

Catalog UI Policy
The laptop type variable becomes visible and mandatory when needs_laptop is Yes.

Catalog Client Script
The client script runs in the browser and displays manager information when the Reporting Manager reference variable changes.

Flow Design
The flow retrieves catalog variables, requests manager approval, handles rejection, creates fulfillment tasks, and conditionally creates a laptop-provisioning task.

Security Note
Client Scripts and Catalog UI Policies improve user experience. They should not be treated as server-side security controls.
