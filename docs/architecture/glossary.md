# Glossary

<!--
Purpose:
Define shared architecture and domain language so business, data, application, technology, and governance artifacts use the same terms.

Use this page for:
- ubiquitous language
- architecture terms with project-specific meaning
- domain terms used across multiple artifacts
- approved synonyms and terms to avoid

Avoid:
- implementation-only class names
- abbreviations that are not used in architecture communication
- long conceptual essays better suited to layer artifacts
-->

## Terms

| Term | Meaning | Context | Preferred Usage | Avoid / Notes |
| --- | --- | --- | --- | --- |
| Architecture Board | Accountable governance group or named owner that accepts architecture decisions, review gates, and waivers. | Governance | Use when an architecture decision needs accountable acceptance. | Do not imply a large committee is required for small teams. |
| Architecture-Significant Requirement | Requirement that can change architecture, integration, security, data ownership, runtime, or governance decisions. | Requirements Management | Track centrally in [Requirements](architecture/requirements.md), then interpret in affected phase artifacts. | Do not use for ordinary feature tasks with no architecture impact. |
| Waiver | Time-boxed accepted deviation from an approved principle, standard, contract, or review gate. | Governance | Record in [Waivers](architecture/governance/waivers.md). | A waiver is not silent technical debt. |
| FairSpot sample: Draw | Process that allocates limited parking capacity to eligible requests according to approved business rules. | Business / Application | Use consistently in business process, API, and event descriptions. | Avoid mixing Draw with generic booking confirmation. |
| FairSpot sample: Allocation | Result of a Draw or direct rule that assigns a parking spot or capacity slot to a request. | Business / Data | Use for the assignment outcome, not the user request itself. | Keep separate from Booking Request. |

## Term Lifecycle

| Status | Meaning |
| --- | --- |
| Proposed | Term is being introduced and needs stakeholder agreement. |
| Approved | Term should be used consistently in architecture artifacts. |
| Deprecated | Term remains for history but should not be used in new content. |
