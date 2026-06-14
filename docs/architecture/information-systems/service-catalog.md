# Service Catalog

<!--
Purpose:
List services, their business capability mapping, owned data, interfaces, and criticality.
-->

| Service | Related Capability | Owned Data | Main Interfaces | Criticality |
| --- | --- | --- | --- | --- |
| Identity / Access | Customer / User Management | Actor context, identity references, authorization inputs | Auth integration, user/context APIs | High |
| Core Domain | Core Domain Operation | Main domain records, lifecycle state, domain decisions | User APIs, operations APIs, domain events | High |
| Read Model / Reporting | Reporting And Insight | Derived projections, report catalog/configuration | Query APIs, report exports, event consumers | Medium |
| Notification | Operations And Support | Notification requests, templates, delivery evidence | Notification APIs, delivery events | Medium |
| Audit | Operations And Support | Audit events and review evidence | Audit APIs, audit exports | High |
