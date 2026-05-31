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

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Gap Analysis</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Baseline Version</strong></td><td style="border:none;padding:3px 0;">Current State v0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Target Version</strong></td><td style="border:none;padding:3px 0;">Target State v0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Phases E/F + Requirements Management</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">—</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">—</td></tr>
</table>

| Gap ID | Area | Baseline Version | Target Version | Baseline State | Target State | Gap | Impact | Work Package | Owner | Status |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| GAP-001 | Durable state | Current State v0.1 | Target State v0.1 | Some operational state is held in memory or lacks restore evidence. | Pilot-critical state is persistent, tenant/domain scoped, and covered by restore evidence. | Persistence and restore posture is incomplete. | Restart or incident can block safe pilot operation. | [Work Packages](../implementation-migration/work-packages.md) | Architecture Owner | Open |
| GAP-002 | API contract evidence | Current State v0.1 | Target State v0.1 | Some APIs are documented narratively. | Generated or source-of-truth contracts are linked from architecture. | Contract evidence is incomplete or hard to find. | Client or service changes can drift unnoticed. | [Work Packages](../implementation-migration/work-packages.md) | Architecture Owner | Planned |
| GAP-003 | Security readiness | Current State v0.1 | Target State v0.1 | Security controls are known but not all validated against deployment profile. | Ingress, identity, secrets, audit, and monitoring are validated for the selected profile. | Deployment-specific security evidence is incomplete. | Public exposure risk remains before go-live. | [Readiness](../implementation-migration/readiness.md) | Security Lead | Open |
| GAP-FS-001 | FairSpot sample: tenant readiness persistence | Current State v0.1 | Customer-Ready Target v0.1 | Some tenant/customer readiness state is in-memory or not yet restart-safe. | Tenant readiness and onboarding state is tenant-scoped, durable, backup-aware, and safe for hosted pilot operation. | Customer pilot cannot rely on volatile state for tenant readiness. | Public customer traffic is blocked until durability and tenant isolation are proven. | [WP-FS-001](../implementation-migration/work-packages.md) | Architecture Owner / Implementer | Planned |

## Gap Status Values

| Status | Meaning |
| --- | --- |
| Open | Gap is known and unresolved. |
| Planned | Gap has an accepted resolution path. |
| In Progress | Work is actively closing the gap. |
| Closed | Evidence shows the gap is closed. |
| Accepted | Gap remains by explicit risk or scope decision. |
