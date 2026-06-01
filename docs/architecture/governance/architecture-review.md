# Architecture Review

<!--
Purpose:
Define how architecture changes are reviewed and accepted.

Use this page for:
- review triggers
- review checklist
- evidence required
- approval roles
- escalation path

Avoid:
- replacing normal code review
- review steps nobody will run
-->

## Review Triggers

- New architecture-significant requirement.
- New bounded context, integration, data store, or deployment profile.
- Security, privacy, compliance, or operational risk change.
- Exception to an approved principle or standard.
- ADM phase gate or architecture version needs acceptance.

## ADM Phase Review Gates

Use [TOGAF ADM Checklist](../adm-checklist.md) as the phase readiness tool. This page defines how the review is run and what evidence reviewers should expect.

| Gate | Review Focus | Typical Evidence |
| --- | --- | --- |
| Preliminary / Phase A | Scope, stakeholders, principles, governance, and architecture vision. | Vision, stakeholders and concerns, principles, artifact register, board model. |
| Phases B/C/D | Business, information systems, technology, security, and requirements interpretation. | Layer artifacts, diagrams, requirements impact, decisions, baseline/target notes. |
| Phases E/F | Gaps, options, transition architectures, work packages, roadmap, and readiness criteria. | Gap analysis, transition states, work packages, roadmap, version register. |
| Phases G/H | Implementation conformance, waivers, change requests, version updates, and residual risks. | PR/release evidence, readiness checks, waivers, change control, decisions. |

## Checklist

- Stakeholder concern is identified.
- Alternatives and rationale are documented.
- Security and privacy impact is considered.
- Operational impact is considered.
- Decision is recorded if durable.
- Requirements, gaps, work packages, and affected artifacts are linked.
- Acceptance, deferral, waiver, or required rework is explicit.

## Outcomes

| Outcome | Meaning | Follow-up |
| --- | --- | --- |
| Accepted | Evidence is sufficient for the stated scope. | Update artifact metadata and version/register status where needed. |
| Accepted With Gaps | Work may proceed, but named gaps remain. | Add or update gap/work-package rows and owners. |
| Deferred | Review cannot conclude because evidence or decision input is missing. | Assign owner for missing evidence or decision. |
| Rework Required | Material contradiction, risk, or missing acceptance criteria blocks progression. | Revise artifacts or implementation before review is accepted. |
