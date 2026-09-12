# Project 2: Technical Notes

## Architecture Diagram (Conceptual)
[Incident Record Created]
│
▼
[Assignment Rules Evaluation]
└── Order 100: VIP Caller → IT Support Team
└── Order 200: Hardware Category → Hardware Support
└── Order 300: Software Category → IT Support Team
└── Order 400: Network Category → Network Support
  │
  ▼
[Business Rules]
└── VIP Caller: Set Impact/Urgency = 1 (Before Insert)
└── P1 Incident: Auto-Log Work Note (After Insert/Update)
[SLA Engine]
└── P1 Response (15 min)
└── P1 Resolution (4 hours)
└── P2 Resolution (8 hours)

## Key Tables Used
| Table | Purpose |
|---|---|
| incident | Primary table for incidents |
| sys_rule_assignment | Assignment Rules |
| sys_script_client | Client Scripts |
| sys_script | Business Rules |
| sla | SLA Definitions |
| task_sla | Task-SLA instances on records |

## Concepts Practiced
- Assignment Rule Order (lower = first match wins)
- Business Rule Triggers (before vs after)
- Client Scripts (onChange)
- SLA Conditions (Start, Stop, Pause)
- GlideRecord updates from Business Rules
