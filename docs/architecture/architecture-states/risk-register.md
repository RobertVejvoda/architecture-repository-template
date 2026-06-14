# Risk Register

<!--
Purpose:
Track architecture-significant risks that are not only security gaps and may affect delivery, operations, integration, data, or stakeholder outcomes.

Use this page for:
- architecture risks with probability, impact, mitigation, and owner
- non-security risks that do not belong in the security gap register
- risks that influence gaps, work packages, standards, or waivers
- review of residual risk before architecture acceptance

Avoid:
- ordinary project task tracking
- duplicating confirmed gaps from Gap Analysis without risk context
- hiding security-specific issues that belong in Security Gap Register
-->

## Risks

| Risk ID | Area | Risk | Probability | Impact | Mitigation | Linked Artifact | Owner | Review Date | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| RISK-001 | Delivery | Architecture artifacts may become too broad to maintain. | Medium | Medium | Keep pages focused, use the artifact register, and review only architecture-significant changes. | [Artifact Register](/architecture/artifact-register.md) | Architecture Owner | YYYY-MM-DD | Open |
| RISK-002 | Integration | API and event contracts can drift from implementation if contract evidence is not linked. | Medium | High | Require contract locations in [API Contracts](/architecture/information-systems/api-contracts.md) and event ownership in [Integrations and Events](/architecture/information-systems/integrations-events.md). | [Technology Standards](/architecture/technology/standards.md) | Architecture Owner | YYYY-MM-DD | Open |
| RISK-003 | Operations | Production use may be blocked if restore, monitoring, and support runbooks are not proven before go-live. | Medium | High | Link readiness evidence to work packages and deployment profile acceptance. | [Readiness](/architecture/implementation-migration/readiness.md) | Platform Owner | YYYY-MM-DD | Open |
| RISK-004 | Ownership | Unclear ownership can leave decisions, data, support, or controls without accountable owners. | Medium | High | Name owners in artifacts and route unresolved questions through Governance Log. | [Architecture Governance Log](/architecture/governance/architecture-governance-log.md) | Architecture Board | YYYY-MM-DD | Open |

## Risk Handling

| Status | Meaning |
| --- | --- |
| Open | Risk is known and needs mitigation, acceptance, or more evidence. |
| Mitigating | Mitigation work is underway or linked to a work package. |
| Accepted | Residual risk is accepted by the accountable owner. |
| Closed | Risk no longer applies or mitigation evidence is complete. |
