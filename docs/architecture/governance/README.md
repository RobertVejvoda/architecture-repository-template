# Governance

<!--
Purpose:
Describe how architecture is reviewed, changed, and governed over time.

Use this page for:
- governance overview
- architecture review process
- architecture contract and conformance expectations
- change control
- waiver handling
- decision ownership

Avoid:
- heavy process where lightweight review is enough
- hidden decision paths
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

## Contents

- [Architecture Board](/architecture/governance/architecture-board.md)
- [Architecture Governance Log](/architecture/governance/architecture-governance-log.md)
- [Architecture Review](/architecture/governance/architecture-review.md)
- [Architecture Contract](/architecture/governance/architecture-contract.md)
- [Architecture Change Set](/architecture/governance/architecture-change-set.md)
- [Change Control](/architecture/governance/change-control.md)
- [Waivers](/architecture/governance/waivers.md)

## Requirement Coverage

Use this section to show how Governance interprets central requirements from [Requirements Management](/architecture/requirements.md). Governance does not redefine the requirement; it defines review, conformance, waiver, and change-control expectations.

| Requirement | Governance Interpretation | Impacted Artifacts | Evidence / Gap |
| --- | --- | --- | --- |
| AR-001 | Reviews must verify that role and organizational scope are covered by architecture artifacts and implementation evidence. | Architecture Review, Architecture Contract, Waivers. | Require explicit waiver or finding for missing authorization evidence. |
| AR-003 | Public-facing ingress, identity, logging, and abuse-prevention choices need architecture review before approval. | Architecture Board, Architecture Review, Change Control. | Record approval, residual risk, or waiver before go-live. |
| AR-004 | Architecture governance separates target state, current evidence, gaps, risks, waivers, and delivery tasks. | Governance Log, Change Set, Version Register. | Route each item to one authoritative artifact. |
