# Architecture Constraints

<!--
Purpose:
Record fixed limits that shape architecture options.

Use this page for:
- externally imposed deadlines
- platform constraints
- regulatory boundaries
- budget limits
- mandatory technology or integration constraints

Avoid:
- duplicating requirements
- recording preferences as constraints
- hiding assumptions inside constraint wording
-->

| Constraint ID | Constraint | Statement | Affected Artifacts | Implication | Owner | Review Trigger | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| CON-001 | Hosting | Initial deployment must fit the approved deployment profiles. | [Runtime Platform](/architecture/technology/runtime-platform.md), [Deployment Profiles](/architecture/technology/deployment-profiles.md) | Architecture choices must match the selected profile or record a waiver. | Architecture Owner | Deployment profile changes. | Draft |
| CON-002 | Data residency | Sensitive data must remain inside approved jurisdictions or environments. | [Data Architecture](/architecture/information-systems/data-architecture.md), [Privacy Architecture](/architecture/security/privacy-architecture.md) | Storage, backup, and support access choices need jurisdiction review. | Security / Privacy Lead | New data store, backup, or external support path. | Draft |
| CON-003 | Operational evidence | Production acceptance requires restore, monitoring, and support evidence. | [Readiness](/architecture/implementation-migration/readiness.md), [Observability](/architecture/technology/observability.md) | Work packages must include evidence, not only implementation. | Operations Lead | Production readiness review. | Draft |

## Constraints, Requirements, And Assumptions

| Item | Meaning | Example |
| --- | --- | --- |
| Constraint | A hard limit that shapes available options. | Must use an approved cloud region. |
| Requirement | What must be true for stakeholders or the architecture to succeed. | Users must only access permitted data and actions. |
| Assumption | Something believed true but not yet proven. | A selected platform service supports the required resiliency profile. |
