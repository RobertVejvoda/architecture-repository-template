# Architecture Governance Log

<!--
Purpose:
Track active board-level architecture questions before they are resolved or routed.

Use this page for:
- architecture questions requiring board or accountable-owner input
- acceptance blockers
- decisions needing evidence before final routing
- questions that may become decisions, gaps, risks, waivers, change sets, or delivery work

Avoid:
- permanent decision history
- local open questions that belong in one artifact
- daily delivery task tracking
-->

The governance log is active intake only. Once an item is resolved, move the final record to the right artifact and remove or close the active log row.

## Governance Log

| ID | Question / Issue | Trigger | Owner | Evidence Needed | Target Review | Status | Route When Resolved |
| --- | --- | --- | --- | --- | --- | --- | --- |
| GOV-001 | Example: Which deployment profile is accepted for the first reviewed target state? | Phase A / Phase D scope question. | Architecture Owner | Candidate comparison, risks, cost, operations evidence. | YYYY-MM-DD | Open | Decision, Target Architecture, Deployment Profiles, Risk Register. |

## Status Values

| Status | Meaning |
| --- | --- |
| Open | Question is active and needs owner/evidence. |
| Evidence Needed | More information is required before review. |
| Ready For Review | Owner believes the item can be decided or routed. |
| Routed | Outcome has been moved to the target artifact. |
| Closed | Item has no remaining architecture action. |

## Routing Rules

| Outcome | Record In |
| --- | --- |
| Durable choice | [Architecture Decisions](/architecture/decisions.md) |
| Missing capability or evidence | [Gap Analysis](/architecture/architecture-states/gap-analysis.md) |
| Uncertainty or exposure | [Risk Register](/architecture/architecture-states/risk-register.md) |
| Time-boxed exception | [Waivers](/architecture/governance/waivers.md) |
| Multi-artifact solution change | [Architecture Change Set](/architecture/governance/architecture-change-set.md) |
| Delivery implementation task | Delivery tool, with links from relevant architecture artifact |
| No architecture impact | Close the log item with a short rationale |
