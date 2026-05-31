# Actors And Roles

<!--
Purpose:
Identify business actors, personas, and role responsibilities.

Use this page for:
- business actors
- role intent
- responsibilities
- high-level access expectations

Avoid:
- detailed IAM policy syntax
- implementation-specific groups unless architecture-relevant
-->

| Actor / Role | Responsibilities | Concerns | Notes |
| --- | --- | --- | --- |
| Employee / End User | Requests resources, views own status, and receives notifications. | Clear outcome, privacy, simple workflow. | Must not see other users' private data. |
| Manager / Operations User | Reviews operational queues, exceptions, and service readiness. | Safe override actions, auditability, timely status. | Access should be scoped by organization or location. |
| Administrator | Configures tenants, policies, integrations, and readiness checks. | Correct setup, traceability, rollback, supportability. | Privileged actions require audit evidence. |
