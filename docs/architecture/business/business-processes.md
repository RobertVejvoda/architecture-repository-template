# Business Processes

<!--
Purpose:
Describe core business processes at enough detail to validate the architecture.

Use this page for:
- process overview
- triggers and outcomes
- major business rules
- exceptions and handoffs
- links to BPMN or other diagrams

Avoid:
- code-level orchestration details
- implementation task lists
-->

| Process | Trigger | Main Outcome | Exceptions |
| --- | --- | --- | --- |
| Tenant Onboarding | New customer or organizational unit must be enabled. | Tenant is configured, validated, and marked ready. | Missing identity setup, failed readiness checks, incomplete policy configuration. |
| Resource Request Fulfilment | User submits a request for a constrained resource. | Request is accepted, allocated, waitlisted, rejected, or cancelled. | Eligibility failure, capacity shortage, late cancellation, manual override. |
| Architecture Change Review | New architecture-significant requirement or risk appears. | Decision, waiver, gap, or work package is recorded. | Missing evidence, unresolved ownership, rejected change. |
