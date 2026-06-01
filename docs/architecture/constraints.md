# Constraints

<!--
Purpose:
Record solution limits that shape architecture choices but are not requirements by themselves.

Use this page for:
- regulatory, contractual, budget, schedule, and technology constraints
- immovable assumptions that limit solution options
- constraints that need review before changing architecture direction
- links from Architecture Vision, Requirements, and Gap Analysis

Avoid:
- duplicating requirements
- recording preferences that can be changed without governance
- hiding risks that belong in the Risk Register
-->

## Constraint Register

| Constraint ID | Type | Constraint | Impacted Artifacts | Rationale | Owner | Review Trigger | Status |
| --- | --- | --- | --- | --- | --- | --- | --- |
| CON-001 | Schedule | Initial architecture must be useful before it is complete. | [ADM Checklist](architecture/adm-checklist.md), [Artifact Register](architecture/artifact-register.md) | Lightweight governance should not block discovery. | Architecture Owner | Before moving an artifact to Approved. | Proposed |
| CON-002 | Technology | Approved runtime and integration choices must be visible before implementation teams depend on them. | [Technology Standards](architecture/technology/standards.md), [Architecture Contract](architecture/governance/architecture-contract.md) | Delivery teams need a clear conformance baseline. | Architecture Owner | New platform, protocol, or runtime choice. | Proposed |
| CON-FS-001 | FairSpot sample: hosting | FairSpot pilot is expected to run on a small hosted footprint before enterprise scaling. | [Runtime Platform](architecture/technology/runtime-platform.md), [Deployment Profiles](architecture/technology/deployment-profiles.md), [Risk Register](architecture/architecture-states/risk-register.md) | Architecture choices should fit the first customer-ready deployment. | Product Owner / Architecture Owner | Hosting profile changes. | Proposed |

## Constraint vs Requirement

| Item | Meaning | Example |
| --- | --- | --- |
| Requirement | What must be true for stakeholders or the architecture to succeed. | System must support tenant isolation. |
| Constraint | Limit that narrows acceptable solution options. | Public deployment must run behind the approved ingress and WAF profile. |
| Risk | Uncertain event or condition that can affect the architecture. | Restore process may not be proven before pilot launch. |
