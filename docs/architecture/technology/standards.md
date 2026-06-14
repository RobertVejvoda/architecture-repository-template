# Technology Standards

<!--
Purpose:
Record approved technology choices, profiles, and exceptions.
-->

| Standard ID | Area | Standard | Applies To | Rationale | Exception Path | Owner | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| STD-001 | Runtime | Prefer platform building blocks where they reduce operational risk and improve portability. | Services, workers, integrations. | Consistent runtime patterns simplify support and conformance review. | Direct bypass needs a decision, rationale, and review. | Architecture Owner | Proposed |
| STD-002 | Ingress | Public-facing surfaces should use the approved protected ingress and abuse-prevention profile. | Public web and API endpoints. | Reduces exposure and centralizes operational controls. | Any public bypass requires a time-boxed [Waiver](/architecture/governance/waivers.md). | Security Lead | Proposed |
| STD-003 | Observability | Services must emit logs, metrics, traces, and health signals appropriate to the selected profile. | Runtime and deployment profiles. | Operations need evidence for support and readiness. | Missing telemetry is tracked as a gap or waiver. | Operations Lead | Proposed |
| STD-004 | Contracts | Architecture-significant APIs and events should have source-of-truth contract evidence. | APIs, events, integrations. | Reduces drift between documentation and implementation. | Narrative-only contracts require an explicit gap. | Architecture Owner | Proposed |
