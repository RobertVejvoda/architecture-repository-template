# Application Architecture

<!--
Purpose:
Describe applications, bounded contexts, modules, and their responsibilities.

Use this page for:
- application components
- service boundaries
- ownership and responsibilities
- main user-facing applications

Avoid:
- deployment topology
- class-level design
-->

| Application / Component | Responsibility | Owner | Interfaces |
| --- | --- | --- | --- |
| Customer / Tenant Service | Owns tenant lifecycle, readiness state, and onboarding metadata. | Customer domain | Admin API, readiness events |
| Booking / Allocation Service | Owns request commands, allocation state, policy decisions, and lifecycle events. | Core product domain | User API, operations API, domain events |
| DataHub / Read Model Service | Owns cross-service read models, projection health, and aggregate query surfaces. | Architecture / analytics domain | Query API, event subscriptions |
