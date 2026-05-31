# Data Architecture

<!--
Purpose:
Describe business data, ownership, persistence, classification, and lifecycle.

Use this page for:
- conceptual data model
- system of record
- read models
- retention and lifecycle
- data classification

Avoid:
- full physical database schema unless architecture-relevant
- temporary migration scripts
-->

| Data Area | Owner | Classification | Lifecycle Notes |
| --- | --- | --- | --- |
| Tenant readiness state | Customer / Tenant Service | Internal / Confidential | Retained while tenant is active; archived or deleted according to contract. |
| Resource requests and outcomes | Booking / Allocation Service | Confidential | Retained for operational, audit, and dispute windows. |
| Projection summaries | DataHub / Read Model Service | Internal / Confidential | Rebuildable from events where event retention permits; freshness and lag tracked. |
