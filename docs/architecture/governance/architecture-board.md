# Architecture Board

<!--
Purpose:
Define the group that accepts architecture direction, validates phase readiness, and records durable decisions.

Use this page for:
- board membership and roles
- quorum and decision rules
- decision and review responsibilities
- escalation and exception handling

Avoid:
- replacing the decision log
- day-to-day delivery assignment
- private personnel details that should not be public
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Cross-cutting</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Preliminary / Phase G / Phase H</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

## Purpose

The Architecture Board provides the lightweight governance body for architecture-significant decisions, phase readiness validation, standards, exceptions, and change control.

## Membership

Replace the example roles with project-specific members or role names.

| Role | Responsibility | Required For Quorum |
| --- | --- | --- |
| Architecture Owner | Maintains architecture repository, prepares decisions, and tracks evidence. | Yes |
| Business Sponsor | Confirms business fit, priorities, and acceptable trade-offs. | Yes |
| Security / Privacy Representative | Reviews trust, compliance, privacy, and risk impact. | For security/privacy-impacting decisions |
| Operations Representative | Reviews deployability, supportability, resilience, and recovery impact. | For production-impacting decisions |
| Delivery Lead | Confirms implementation feasibility and migration impact. | When delivery plan changes |

## Decision Rules

- Durable architecture decisions are recorded in [Architecture Decisions](../decisions.md).
- Each decision should identify the decision maker, date, status, rationale, alternatives considered, and affected artifacts.
- Phase progression should not be treated as accepted until required artifacts are at `In Review` or stronger and material gaps are either planned, accepted, or closed.
- Exceptions are recorded in [Waivers](waivers.md), not hidden in meeting notes.
- Architecture-significant changes after approval are handled through [Change Control](change-control.md).

## Decision Status Values

| Status | Meaning |
| --- | --- |
| Proposed | Decision is drafted but not accepted. |
| Accepted | Decision is approved for the stated scope. |
| Superseded | Decision was replaced by a newer decision. |
| Deprecated | Decision remains historically useful but should not guide new work. |
| Rejected | Option was considered and explicitly not selected. |

## Review Cadence

| Review Type | When | Evidence |
| --- | --- | --- |
| Phase readiness review | Before moving to the next ADM phase or accepting a phase bundle. | Artifact metadata, gap analysis, requirements impact, decisions. |
| Architecture change review | When an approved target, principle, standard, or requirement changes. | Change request, affected artifacts, decision record. |
| Implementation conformance review | During Phase G or release readiness. | PR/release evidence, readiness checks, unresolved gaps. |
| Periodic architecture review | Project-defined cadence or major business/technology trigger. | Updated artifact register and version register. |

## FairSpot Samples

| Decision | Board Consideration | Recorded In |
| --- | --- | --- |
| Use Dapr-first runtime building blocks where they fit production needs. | Portability across NAS, demo, and future hosted profiles; need explicit gaps where Dapr features are unsupported or unvalidated. | Architecture Decisions, Runtime Platform, Gap Analysis. |
| Track tenant isolation as a cross-phase architecture requirement. | Affects business processes, API contracts, persistence, events, read models, deployment profiles, security controls, and implementation review. | Requirements, phase artifacts, Gap Analysis, Work Packages. |
