# Architecture Decisions

<!--
Purpose:
Provide a decision log or link to the project's canonical Architecture Decision Record location.

Use this page for:
- durable architecture choices
- rejected alternatives
- decision owner and date
- consequences

Avoid:
- temporary implementation notes
- decisions without rationale
-->

Architecture Board decisions are recorded here. Board membership, quorum, and review responsibilities are defined in [Architecture Board](architecture/governance/architecture-board.md).

| Decision ID | Decision | Rationale | Decision Maker | Date | Status | Related Artifacts |
| --- | --- | --- | --- | --- | --- | --- |
| ADR-001 | Use service-owned writes with read-model projections for cross-service queries. | Keeps command ownership clear while supporting reporting and operational views without direct reads from private service stores. | Architecture Board | YYYY-MM-DD | Proposed | Data Architecture, Integrations and Events, Work Packages |
| ADR-002 | Treat tenant isolation as a cross-phase architecture requirement. | Tenant isolation affects business processes, APIs, persistence, events, runtime configuration, security controls, and implementation review. | Architecture Board | YYYY-MM-DD | Proposed | Requirements, Security Architecture, Gap Analysis |
| ADR-003 | Keep generated API contracts authoritative where available. | Reduces drift between implementation, clients, and architecture documentation; narrative docs explain intent but do not override generated contracts. | Architecture Owner | YYYY-MM-DD | Proposed | API Contracts, Application Architecture |
