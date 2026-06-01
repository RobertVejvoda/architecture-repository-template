# Technology Standards

<!--
Purpose:
Define approved technology choices and standards that implementation teams should follow unless a waiver is accepted.

Use this page for:
- approved platforms, protocols, runtimes, libraries, and integration standards
- standard versions and review triggers
- deviation rules
- links to waivers and architecture contracts

Avoid:
- environment secrets
- every dependency in a software bill of materials
- local developer preferences that do not affect architecture
-->

## Approved Standards

| Standard ID | Area | Approved Standard | Version / Profile | Applies To | Deviation Rule | Owner | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| STD-001 | API | HTTP APIs with documented contracts and compatibility rules. | Project-defined | Public and internal service APIs. | Changes that break compatibility need [Architecture Review](architecture/governance/architecture-review.md). | Architecture Owner | Proposed |
| STD-002 | Events | Events must have stable names, versioning rules, ownership, and replay/idempotency expectations. | Project-defined | Integration and read-model events. | Missing ownership or versioning needs a gap or waiver before production use. | Architecture Owner | Proposed |
| STD-003 | Observability | Services expose health, logs, metrics, and trace correlation appropriate to the deployment profile. | Project-defined | Runtime services and background workers. | Missing production evidence belongs in [Risk Register](architecture/architecture-states/risk-register.md) or [Gap Analysis](architecture/architecture-states/gap-analysis.md). | Platform Owner | Proposed |
| STD-FS-001 | FairSpot sample: runtime | Platform building blocks are preferred where they reduce operational risk. | Target profile | FairSpot runtime. | Direct integration needs a decision, rationale, and review. | Architecture Owner | Proposed |
| STD-FS-002 | FairSpot sample: ingress | Public customer access should use the approved protected ingress and WAF profile. | Pilot / production profile | Public web and API endpoints. | Any public bypass requires a time-boxed [Waiver](architecture/governance/waivers.md). | Security Lead | Proposed |

## Review Rules

- Review standards when a runtime, platform, protocol, or integration pattern changes.
- Link accepted deviations to [Waivers](architecture/governance/waivers.md).
- Reflect binding standards in the [Architecture Contract](architecture/governance/architecture-contract.md).
