# Architecture Repository

<!--
Purpose:
Use this page as the main architecture repository index. It should help a new reader find the current target architecture, important decisions, architecture views, and known gaps.

Use this page for:
- architecture scope and repository rules
- links to ADM phase artifacts
- authoritative diagram/view indexes
- decision log and governance entry points

Avoid:
- duplicating detailed content from child pages
- implementation task tracking unless needed for architecture governance
-->

## Repository Scope

Describe what the architecture repository covers and which systems, products, organizations, domains, or architecture cycles are in scope.

State important exclusions clearly. A reader should know whether this repository covers product architecture, enterprise architecture, solution architecture, migration governance, implementation conformance, or only a subset.

## Current Architecture Focus

| ADM Area | Current Goal | Status |
| --- | --- | --- |
| Preliminary | Establish principles, governance, repository rules, risk tracking, and review gates. | Draft |
| Phase A | Define problem statement, goals, non-goals, stakeholders, constraints, and architecture vision. | Draft |
| Phase B | Use business capabilities, value streams, processes, actors, and policies as the backbone for requirements. | Draft |
| Phase C | Define application, data, integration, API, event, and service boundaries. | Placeholder |
| Phase D | Define runtime, deployment, observability, and technology standards. | Placeholder |
| E/F | Define candidate options, transition states, gaps, risks, roadmap, and work packages. | Placeholder |
| G/H | Define implementation conformance, waivers, governance log, change sets, and change management. | Placeholder |

## Architecture Areas

| Area | Purpose |
| --- | --- |
| [Architecture In Plain Words](/architecture/plain-language-introduction.md) | Simple explanation for new readers and reviewers, including how to work with the repository. |
| [Architecture Vision](/architecture/architecture-vision.md) | Why the architecture exists and what outcome it supports. |
| [Principles](/architecture/principles.md) | Stable decision rules for architecture choices. |
| [Stakeholders and Concerns](/architecture/stakeholders-and-concerns.md) | Stakeholder catalog, concerns, viewpoints, and validation questions. |
| [Requirements](/architecture/requirements.md) | Architecture-significant requirements with traceability to affected phases and evidence. |
| [Constraints](/architecture/constraints.md) | Hard limits and externally imposed boundaries that shape options. |
| [Business Architecture](/architecture/business/README.md) | Business capabilities, value streams, actors, processes, and policies. |
| [Information Systems](/architecture/information-systems/README.md) | Application, data, service, API, integration, event, and read-model architecture. |
| [Technology Architecture](/architecture/technology/README.md) | Runtime, deployment, observability, approved standards, and operational profiles. |
| [Security Architecture](/architecture/security/README.md) | Security, privacy, controls, trust boundaries, and known gaps. |
| [Architecture States](/architecture/architecture-states/README.md) | Baseline, candidate, target, transition states, gap analysis, risk register, and version register. |
| [Implementation And Migration](/architecture/implementation-migration/README.md) | Migration roadmap, work packages, delivery sourcing options, increment checklist, and readiness. |
| [Governance](/architecture/governance/README.md) | Architecture board, governance log, review, contract, change set, change control, and waivers. |
| [Views And Diagrams](/architecture/views/README.md) | Viewpoint catalog and diagram register. |
| [Repository Changes](/architecture/repository-changes.md) | Repository-structure changes that affect navigation or governance interpretation. |

## Repository Rules

- Keep each artifact to one job.
- Prefer links over duplication.
- Record durable decisions in [Architecture Decisions](/architecture/decisions.md).
- Track requirements centrally in [Requirements](/architecture/requirements.md), then interpret them in affected phase artifacts.
- Put unvalidated solution options in [Candidate Architectures](/architecture/architecture-states/candidate-architectures.md), not directly in target architecture.
- Keep target architecture separate from baseline evidence, transition states, open gaps, risks, and implementation evidence.
- Track architecture versions in [Architecture Version Register](/architecture/architecture-states/architecture-version-register.md).
- Use [Architecture Change Set](/architecture/governance/architecture-change-set.md) when a material solution change affects several artifacts.
- Use [Architecture Governance Log](/architecture/governance/architecture-governance-log.md) only for active board-level questions. Move resolved items to decisions, gaps, risks, waivers, change sets, or delivery tooling.
- Keep delivery tasks, sprint state, and day-to-day assignments in the delivery tool, not in Markdown.

## Assumption Placement

| If An Assumption Is | Put It In |
| --- | --- |
| About a candidate option | [Candidate Architectures](/architecture/architecture-states/candidate-architectures.md) |
| About current-state evidence | [Baseline Architecture](/architecture/architecture-states/baseline-architecture.md) |
| About the accepted target state | [Target Architecture](/architecture/architecture-states/target-architecture.md) |
| Effectively fixed and limits options | [Constraints](/architecture/constraints.md) |
| Uncertain and harmful if wrong | [Risk Register](/architecture/architecture-states/risk-register.md) |
| Resolved by choosing one path | [Architecture Decisions](/architecture/decisions.md) |
