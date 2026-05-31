# Architecture Requirements

<!--
Purpose:
Track architecture-significant requirements and trace them to ADM phases, views, decisions, gaps, and work packages.

Use this page for:
- non-functional requirements
- cross-cutting business requirements
- regulatory/security requirements
- requirements that affect more than one architecture phase
- traceability to phase artifacts, decisions, gaps, and work packages

Avoid:
- full product backlog duplication
- detailed user stories unless architecture-significant
- copying the same requirement into every phase artifact as a competing duplicate
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Cross-cutting</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Requirements Management</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

Requirements Management is continuous across the ADM. Requirements are captured centrally here, then each affected phase explains how it interprets and satisfies the requirement in its own artifact.

## Requirement Register

Keep requirement statements generic enough to remain stable. The affected phases make them concrete.

| ID | Requirement | Source | Affected ADM Areas | Status |
| --- | --- | --- | --- | --- |
| AR-001 | Example architecture requirement. | Stakeholder / regulation / strategy | B, C, D, Security, G | Draft |
| AR-FS-001 | FairSpot example: tenant data must be isolated across APIs, persistence, events, audit, and read models. | Customer/security concern | B, C, D, Security, G | Example |

## Phase Impact Tracking

Use this table to show how one requirement is handled across phases. Link to the phase artifact section, gap, work package, or decision that proves the requirement is being addressed.

| Requirement | ADM Area | Phase Interpretation | Evidence | Gap / Work |
| --- | --- | --- | --- | --- |
| AR-FS-001 | Phase B - Business Architecture | Business roles and processes must not expose or act on another tenant's requests, people, policy, or reports. | Business roles, business processes, policies. | HR cancellation authorization validation. |
| AR-FS-001 | Phase C - Information Systems | APIs derive tenant/user from authenticated context; services own tenant-scoped data; events and read models carry tenant context safely. | Application architecture, data architecture, API contracts, event contracts. | DataHub projection isolation evidence. |
| AR-FS-001 | Phase D - Technology Architecture | Runtime components, state stores, pub/sub topics, secrets, and deployment profiles preserve tenant boundaries. | Runtime platform, deployment profiles. | Deployment-profile-specific component validation. |
| AR-FS-001 | Security / Privacy | Authorization, audit, privacy, encryption, and data-minimisation controls protect tenant and employee data. | Security architecture, privacy architecture, controls. | Residual risk or waiver if any. |
| AR-FS-001 | Phase G - Implementation Governance | PRs and validation evidence must show tenant-safe API, storage, event, and projection behavior. | Architecture review, readiness evidence, linked PRs. | Open implementation issue or failed validation if any. |

## ADM Area Usage

| ADM Area | How It Uses Requirements |
| --- | --- |
| Preliminary | Defines how requirement changes are governed, reviewed, accepted, or waived. |
| Phase A - Architecture Vision | Identifies stakeholder needs, scope, success measures, and initial architecture-significant requirements. |
| Phase B - Business Architecture | Interprets requirements as capabilities, value streams, actors, processes, and policies. |
| Phase C - Information Systems | Interprets requirements as application boundaries, data ownership, APIs, events, integrations, and read models. |
| Phase D - Technology Architecture | Interprets requirements as runtime, deployment, platform, observability, backup, and operational needs. |
| Phases E/F | Converts requirement gaps into solution increments, transition architectures, work packages, and migration plans. |
| Phase G | Verifies implementation evidence against accepted requirements and architecture constraints. |
| Phase H | Revises requirements when operating evidence, customer feedback, risk, or assumptions change. |
| Security / Privacy | Applies cross-cutting controls and accepted-risk decisions wherever requirements affect trust, compliance, or sensitive data. |

## Tracking Rules

- Add a new row here first when a requirement is architecture-significant or cross-phase.
- Keep the central requirement generic; do not encode phase-specific implementation details in the main statement.
- Add phase-impact rows for every affected ADM area.
- Update phase artifacts with their interpretation and link back to the requirement ID.
- Link gaps, work packages, decisions, and validation evidence as they appear.
- Revisit this page at the end of each ADM phase and during Phase H change management.
