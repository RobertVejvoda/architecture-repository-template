# Gap Analysis

<!--
Purpose:
Compare baseline and target architecture versions and identify gaps that must be closed.

Use this page for:
- baseline-to-target comparison
- capability, data, application, technology, security, and governance gaps
- gap impact and priority
- link to work packages or decisions

Avoid:
- unowned gaps
- vague improvement ideas without baseline/target comparison
-->

| Gap ID | Area | Baseline Version | Target Version | Baseline State | Target State | Gap | Impact | Work Package | Owner | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GAP-001 | Durable state | Current State v0.1 | Target State v0.1 | Some operational state is held in memory or lacks restore evidence. | Pilot-critical state is persistent, scoped, and covered by restore evidence. | Persistence and restore posture is incomplete. | Restart or incident can block safe pilot operation. | [Work Packages](/architecture/implementation-migration/work-packages.md) | Architecture Owner | Open |
| GAP-002 | API contract evidence | Current State v0.1 | Target State v0.1 | Some APIs are documented narratively. | Generated or source-of-truth contracts are linked from architecture. | Contract evidence is incomplete or hard to find. | Client or service changes can drift unnoticed. | [Work Packages](/architecture/implementation-migration/work-packages.md) | Architecture Owner | Planned |
| GAP-003 | Security readiness | Current State v0.1 | Target State v0.1 | Security controls are known but not all validated against deployment profile. | Ingress, identity, secrets, audit, and monitoring are validated for the selected profile. | Deployment-specific security evidence is incomplete. | Public exposure risk remains before go-live. | [Readiness](/architecture/implementation-migration/readiness.md) | Security Lead | Open |

## Gap Status Values

| Status | Meaning |
| --- | --- |
| Open | Gap is known and unresolved. |
| Planned | Gap has an accepted resolution path. |
| In Progress | Work is actively closing the gap. |
| Closed | Evidence shows the gap is closed. |
| Accepted | Gap remains by explicit risk or scope decision. |
