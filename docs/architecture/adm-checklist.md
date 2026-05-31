# TOGAF ADM Checklist (Lightweight)

This is a practical, non-bureaucratic guide for working through the ADM cycle using this repository. Skip or adapt any step that doesn't fit your context. The goal is *useful architecture*, not complete documentation.

> **How to use this:** Work through each phase in order. For each phase, answer the key questions and update the linked pages. You don't need to finish a phase perfectly before moving on — iterate.

---

## Before You Start — Repository Setup

- [ ] Define repository scope in [Architecture Repository](architecture/README.md): what systems, products, or domains are in scope?
- [ ] Record your tailoring decisions in [TOGAF ADM Map](architecture/togaf-adm-map.md): which phases and artifacts apply, which are intentionally skipped?
- [ ] Set up [Principles](architecture/principles.md) early — they inform every other phase.
- [ ] Assign an owner to the [Artifact Register](architecture/artifact-register.md) to track status.

---

## Preliminary Phase — *Set up the framework*

**Goal:** Agree on how architecture will be done before doing it.

- [ ] What governance model applies? Who can approve and change architecture decisions? → [Governance](architecture/governance/README.md)
- [ ] What are the guiding architecture principles? → [Principles](architecture/principles.md)
- [ ] What tools, formats, and review process will be used? → [Architecture Review](architecture/governance/architecture-review.md)

**Done when:** Team agrees on how decisions are made and recorded.

---

## Phase A — Architecture Vision — *Why are we doing this?*

**Goal:** Establish scope, stakeholders, and a clear target outcome.

- [ ] What problem are we solving, and for whom? → [Architecture Vision](architecture/architecture-vision.md)
- [ ] Who are the stakeholders and what do they care about? → [Stakeholders and Concerns](architecture/stakeholders-and-concerns.md)
- [ ] What are the key constraints (time, budget, regulation, existing systems)?
- [ ] What does success look like?

**Done when:** Sponsor or product owner can read the vision and confirm it matches their intent.

---

## Phase B — Business Architecture — *What does the business need?*

**Goal:** Understand capabilities, processes, and actors well enough to design the right system.

- [ ] What capabilities must exist for the business to operate? → [Capabilities](architecture/business/capabilities.md)
- [ ] What are the key value streams or business processes? → [Value Streams](architecture/business/value-streams.md), [Business Processes](architecture/business/business-processes.md)
- [ ] Who are the actors (users, systems, organisations) involved? → [Actors and Roles](architecture/business/actors-roles.md)
- [ ] Are there relevant policies or rules that constrain design? → [Policies](architecture/business/policies.md)

**Done when:** You can describe what the business does without referencing any technology.

---

## Phase C — Information Systems Architecture — *What does the system do?*

**Goal:** Define applications, data, and integrations at an appropriate level of detail.

- [ ] What applications or services exist or need to exist? → [Application Architecture](architecture/information-systems/application-architecture.md)
- [ ] What are the key data entities and ownership rules? → [Data Architecture](architecture/information-systems/data-architecture.md)
- [ ] How do systems integrate? What APIs and events are involved? → [Integrations and Events](architecture/information-systems/integrations-events.md), [API Contracts](architecture/information-systems/api-contracts.md)

**Done when:** A developer joining the team can understand system boundaries and data flows.

---

## Phase D — Technology Architecture — *How does it run?*

**Goal:** Define the runtime platform and deployment model.

- [ ] What is the deployment and hosting model? → [Runtime Platform](architecture/technology/runtime-platform.md)
- [ ] What are the technology standards and approved components? → [Deployment Profiles](architecture/technology/deployment-profiles.md)
- [ ] How is the system observed in production? → [Observability](architecture/technology/observability.md)

**Done when:** Ops and platform teams can understand what they need to provision and support.

---

## Phase E — Opportunities and Solutions — *What are the gaps and options?*

**Goal:** Compare where you are now with where you need to be, and identify how to get there.

- [ ] Document the current (baseline) state → [Baseline Architecture](architecture/architecture-states/baseline-architecture.md)
- [ ] Document the desired (target) state → [Target Architecture](architecture/architecture-states/target-architecture.md)
- [ ] Identify gaps between baseline and target → [Gap Analysis](architecture/architecture-states/gap-analysis.md)
- [ ] Define candidate solution increments or transition states → [Transition Architectures](architecture/architecture-states/transition-architectures.md)

**Done when:** You can explain the delta between now and the target, and name at least one realistic path.

---

## Phase F — Migration Planning — *How do we sequence the work?*

**Goal:** Turn gaps and solution increments into a deliverable roadmap.

- [ ] Group work into implementable packages → [Work Packages](architecture/implementation-migration/work-packages.md)
- [ ] Sequence the work into a roadmap → [Roadmap](architecture/implementation-migration/roadmap.md)
- [ ] Assess team and organisational readiness → [Readiness](architecture/implementation-migration/readiness.md)
- [ ] Tag architecture versions to delivery milestones → [Architecture Version Register](architecture/architecture-states/architecture-version-register.md)

**Done when:** Delivery lead can read the roadmap and plan sprints or quarters.

---

## Phase G — Implementation Governance — *Are we building what we designed?*

**Goal:** Keep architecture honest during delivery.

- [ ] Are review gates defined? Who signs off architecture compliance? → [Architecture Review](architecture/governance/architecture-review.md)
- [ ] Are deviations from the architecture being tracked? → [Change Control](architecture/governance/change-control.md)
- [ ] Are waivers being recorded with justification? → [Waivers](architecture/governance/waivers.md)

**Done when:** The team knows how to raise and resolve architecture issues without blocking delivery.

---

## Phase H — Architecture Change Management — *How do we evolve it?*

**Goal:** Keep the architecture alive as reality changes.

- [ ] How are change requests to the architecture assessed? → [Change Control](architecture/governance/change-control.md)
- [ ] Are exceptions and waivers time-boxed and reviewed? → [Waivers](architecture/governance/waivers.md)
- [ ] Is the architecture version history up to date? → [Architecture Version Register](architecture/architecture-states/architecture-version-register.md)

**Done when:** Architecture changes go through a lightweight review rather than being silently adopted or ignored.

---

## Requirements Management — *Cross-cutting, always active*

**Goal:** Track architecture-significant requirements so each phase has clear acceptance criteria.

- [ ] Are requirements generic and phase-independent? → [Requirements](architecture/requirements.md)
- [ ] Does each requirement link to the phase artifact that satisfies it?
- [ ] Are gaps and open questions recorded rather than left implicit?

**Tip:** Requirements Management is not a phase — keep it updated throughout the entire ADM cycle.

---

## Lightweight Completion Criteria

A phase is good enough to move on when:

- Key questions are answered (even if partially).
- Assumptions and open questions are written down, not hidden.
- At least one stakeholder from the relevant group has reviewed it.
- The [Artifact Register](architecture/artifact-register.md) reflects current status.

You don't need perfect documentation. You need *enough* documentation that the next person can pick it up.
