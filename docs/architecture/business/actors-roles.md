# Actors And Roles

<!--
Purpose:
Describe business actors and roles at the level needed for architecture decisions.
-->

| Actor / Role | Responsibility | Architecture-Significant Concerns | Notes |
| --- | --- | --- | --- |
| End User | Uses the product or service to complete a business outcome. | Simple journey, correct authorization, understandable status, privacy. | Replace with project-specific user roles. |
| Business Operator | Manages exceptions, operational rules, support actions, or approvals. | Auditability, segregation of duties, clear ownership, traceable changes. | Name specific operator roles when known. |
| Administrator | Configures users, organizations, policies, integrations, or readiness checks. | Privileged access, rollback, validation, supportability. | Privileged actions require audit evidence. |
| Sponsor / Owner | Funds or accepts architecture direction and trade-offs. | Value, risk, cost, timing, acceptance evidence. | Usually accountable for major target decisions. |
| External Reviewer | Reviews architecture for security, compliance, operations, procurement, or customer acceptance. | Evidence, traceability, open gaps, residual risks. | Include only when relevant. |
