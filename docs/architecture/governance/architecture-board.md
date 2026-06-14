# Architecture Board

<!--
Purpose:
Define the group that accepts architecture direction, validates phase readiness, and records durable decisions.
-->

## Purpose

The Architecture Board provides the lightweight governance body for architecture-significant decisions, phase readiness validation, standards, exceptions, and change control.

The board owns acceptance rules. The [TOGAF ADM Checklist](/architecture/adm-checklist.md) is the working checklist for phase readiness, and [Architecture Review](/architecture/governance/architecture-review.md) defines the review process.

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

- Durable architecture decisions are recorded in [Architecture Decisions](/architecture/decisions.md).
- Active board-level questions are tracked in [Architecture Governance Log](/architecture/governance/architecture-governance-log.md) until routed.
- Each decision should identify the decision maker, date, status, rationale, alternatives considered, and affected artifacts.
- Phase progression should not be treated as accepted until required artifacts are at `In Review` or stronger and material gaps are either planned, accepted, or closed.
- Phase gates should use the review gates in [TOGAF ADM Checklist](/architecture/adm-checklist.md) and record the outcome through [Architecture Review](/architecture/governance/architecture-review.md).
- Exceptions are recorded in [Waivers](/architecture/governance/waivers.md), not hidden in meeting notes.
- Material architecture changes after approval are handled through [Architecture Change Set](/architecture/governance/architecture-change-set.md) and [Change Control](/architecture/governance/change-control.md).

## Decision Status Values

| Status | Meaning |
| --- | --- |
| Proposed | Decision is drafted but not accepted. |
| Accepted | Decision is approved for the stated scope. |
| Superseded | Decision was replaced by a newer decision. |
| Deprecated | Decision remains historically useful but should not guide new work. |
| Rejected | Option was considered and explicitly not selected. |

## Review Cadence

| Moment | Practical Rhythm | Main Question |
| --- | --- | --- |
| Architecture assessment is active. | Every 2 weeks, or weekly if blocked. | Are target options, risks, gaps, and evidence moving? |
| Things are stable. | Monthly or project-defined cadence. | Are there open decisions, risks, waivers, or changes needing attention? |
| A phase gate or architecture version needs acceptance. | As needed. | Can this architecture state be accepted? |
| A release or increment is approaching production. | At the release or increment gate. | Does it conform, and can the organization operate it? |
| Something urgent appears. | Within a few business days, based on risk. | What decision or risk acceptance is needed? |

The board should produce one of these outputs:

- decision recorded in Decisions;
- question left active in Governance Log;
- risk recorded in Risk Register;
- gap recorded in Gap Analysis;
- exception recorded in Waivers;
- change impact checked through Change Set;
- delivery action sent to the delivery tool.
