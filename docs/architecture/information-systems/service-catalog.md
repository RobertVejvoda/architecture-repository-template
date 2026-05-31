# Service Catalog

<!--
Purpose:
Catalog services and their architecture responsibilities.

Use this page for:
- service name
- business capability supported
- owned data
- APIs/events
- operational criticality

Avoid:
- deployment instance lists
- low-level endpoint documentation
-->

| Service | Capability | Owns Data | Exposes | Criticality |
| --- | --- | --- | --- | --- |
| Customer | Tenant Onboarding | Tenant lifecycle, readiness, setup metadata | Tenant/admin APIs, readiness events | High |
| Booking | Resource Allocation | Requests, allocations, decisions, lifecycle events | User APIs, operations APIs, booking events | High |
| DataHub | Operational Visibility | Read models, projection health, aggregate summaries | Query APIs, dashboard/report data | Medium/High |
