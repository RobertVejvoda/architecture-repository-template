# Data Architecture

<!--
Purpose:
Describe data ownership, classification, lifecycle, read models, and evidence needs.
-->

| Data Area | Owner | Classification | Lifecycle / Retention | Notes |
| --- | --- | --- | --- | --- |
| User and access context | Identity / Access Service | Confidential | Retained according to identity and audit requirements. | Use least privilege and scope-aware reads. |
| Core domain records | Core Domain Service | Confidential | Retained for operational, audit, and dispute windows. | Authoritative writes belong to the owning service. |
| Derived read models | Read Model / Reporting Service | Internal / Confidential | Rebuildable from source events or synchronized sources where possible. | Track freshness, lineage, and rebuild limits. |
| Audit evidence | Audit Service | Confidential / Restricted | Retained according to legal, security, and operational policy. | Prevent modification by normal operators. |

## Data Rules

- Name the authoritative owner for each important data area.
- Separate command/write data from derived read models.
- Record retention, privacy, export, and deletion expectations.
- Link gaps where persistence, restore, lineage, or freshness evidence is missing.
