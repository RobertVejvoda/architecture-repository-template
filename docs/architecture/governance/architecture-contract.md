# Architecture Contract

<!--
Purpose:
Define the lightweight conformance agreement between architecture governance and delivery teams.

Use this page for:
- architecture conformance expectations
- delivery commitments to approved principles, standards, contracts, and review gates
- evidence required during implementation governance
- violation, waiver, and change handling

Avoid:
- replacing delivery plans or team working agreements
- legal contract language unless an external governance process requires it
- adding process that will not be used
-->

## Contract Scope

Use this artifact when implementation work needs an explicit conformance baseline. Small teams can treat this as the lightweight agreement behind Phase G architecture governance rather than a formal signed document.

## Conformance Expectations

| Contract Item | Expected Conformance | Evidence | Exception Path | Owner |
| --- | --- | --- | --- | --- |
| Approved principles | Delivery choices should follow accepted [Principles](/architecture/principles.md). | Pull request notes, decisions, review evidence. | Record a decision or [Waiver](/architecture/governance/waivers.md). | Architecture Owner |
| Approved technology standards | Runtime, API, event, observability, and ingress choices should follow [Technology Standards](/architecture/technology/standards.md). | Architecture review, deployment profile, contract links. | Waiver or change request before production exposure. | Architecture Owner / Platform Owner |
| API and event contracts | Interfaces should match documented contracts and event ownership. | Contract evidence and compatibility note. | Change control if behavior or compatibility changes. | Architecture Owner |
| Security and privacy controls | Controls should match [Security Architecture](/architecture/security/security-architecture.md), [Privacy Architecture](/architecture/security/privacy-architecture.md), and [Controls](/architecture/security/controls.md). | Security review evidence and gap status. | Security waiver with owner and expiry. | Security Lead |
| Residual risks and gaps | Open risks and gaps should have owner, mitigation, and review date. | [Risk Register](/architecture/architecture-states/risk-register.md), [Gap Analysis](/architecture/architecture-states/gap-analysis.md). | Architecture Board acceptance or rework. | Architecture Owner |

## Review Outcome

| Outcome | Meaning | Required Follow-up |
| --- | --- | --- |
| Conformant | Delivery evidence satisfies the contract for the reviewed scope. | Update review date and relevant artifact status. |
| Conformant With Accepted Gaps | Work may proceed with named residual gaps or risks. | Link gaps, risks, waivers, and owners. |
| Non-Conformant | Material contract expectation is not met. | Rework, change request, or waiver before acceptance. |
