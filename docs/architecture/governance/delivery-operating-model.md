# Delivery Operating Model

<!--
Purpose:
Define architecture expectations for the selected delivery model.

Use this page for:
- delivery-model governance expectations after sourcing is selected
- internal and external architecture responsibilities
- handover and run-readiness expectations
- policy, security, deployment, and support conformance

Avoid:
- replacing procurement contracts
- replacing delivery tracking
- duplicating team ceremonies, sprint plans, or staffing plans
-->

Delivery sourcing may be internal, external, or mixed. Candidate options can be maintained in [Delivery Sourcing Options](/architecture/implementation-migration/delivery-sourcing-options.md), and unresolved sourcing questions can be tracked in the [Architecture Governance Log](/architecture/governance/architecture-governance-log.md).

This page defines governance expectations that any selected option must satisfy before production acceptance. Option-specific details should be completed after the sourcing decision is recorded.

## Decision-Dependent Model

| Aspect | To Be Defined When Sourcing Is Selected |
| --- | --- |
| Delivery structure | Internal delivery, external fixed-scope/fixed-price delivery, internal-led mixed team, or another selected model. |
| External role | Delivery capacity, specialist advice, fixed-scope accountability, managed service, or no external role. |
| Internal role | Product direction, business context, architecture acceptance, deployment readiness, operations readiness, and long-term maintainability. |
| Team boundary | Delivery scope, decision rights, review responsibilities, and escalation route. |
| Handover model | Evidence that accountable staff can operate and evolve the accepted scope. |
| Acceptance model | Architecture conformance plus option-specific readiness and handover evidence. |

## Delivery Expectations

| Area | Expectation |
| --- | --- |
| Conformance | Use accepted principles, standards, controls, contracts, and deployment profiles. |
| Internal onboarding | Involve accountable staff in design, review, deployment rehearsal, incident scenarios, and handover. |
| Knowledge ownership | Name an accountable technical owner for each accepted capability. |
| Deployment model | Fit the accepted build, release, configuration, observability, backup, restore, and rollback model. |
| Policy adoption | Follow security, privacy, access, audit, change, release, and operational policies or record waivers. |
| Evidence | Link reviews, test results, deployment logs, runbooks, restore tests, access reviews, and operational sign-off. |
| Handover | Show that accountable staff can build, deploy, monitor, support, and change the capability. |
| Supplier transition | Record remaining operational, licensing, access, data, or knowledge dependency on external staff. |

## Scrum Team Guidance

Scrum is a delivery execution model. TOGAF is an architecture governance and decision model. They should reinforce each other: architecture provides guardrails and traceability, while Scrum delivers increments and exposes implementation feedback.

| TOGAF / Architecture Concern | Scrum Reflection |
| --- | --- |
| Architecture Vision | Product vision, goals, roadmap themes, and desired outcomes. |
| Architecture Requirements | Backlog items, acceptance criteria, quality attributes, and enabler work. |
| Target Architecture | Architectural runway, guardrails, reference designs, and accepted target-state constraints. |
| Gap Analysis | Epics, enablers, technical debt, migration tasks, risks, and dependency work. |
| Work Packages / Roadmap | Epics, releases, increments, milestones, or sprintable vertical slices. |
| Architecture Governance | Definition of Ready, Definition of Done, architecture review, conformance checks, and accepted waivers. |
| Change Management | Backlog refinement, implementation feedback, operating feedback, and architecture change sets. |

Scrum backlog items are not the architecture source of truth. Architecture-significant requirements, decisions, constraints, target states, risks, gaps, controls, waivers, and conformance expectations belong in the architecture repository and should be linked from delivery work.

Watch for these failure modes:

- treating sprint tickets as durable architecture decisions;
- hiding non-functional requirements inside user stories without central traceability;
- letting each sprint make local architecture choices that drift from the target state;
- using architecture as a one-time upfront phase and then ignoring implementation feedback;
- skipping architecture governance because the team is Agile;
- making architects external approvers instead of continuous contributors to refinement, review, and acceptance.

For Scrum teams, a delivery slice is ready when the relevant architecture guardrails are known or explicitly marked as open questions. A slice is done when it works, has evidence, and conforms to the accepted architecture or has an accepted waiver.

## Acceptance Gate

Delivered scope should not be accepted for production use until:

- delivery sourcing option is selected and recorded where relevant;
- architecture conformance has been reviewed through [Architecture Contract](/architecture/governance/architecture-contract.md);
- accountable ownership is named and accepted;
- required standards, controls, and deployment profile are satisfied or waived;
- handover and operational readiness evidence are linked;
- residual supplier or capacity dependencies are recorded as gaps, risks, decisions, or waivers.
