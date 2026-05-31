# TOGAF ADM Map

<!--
Purpose:
Map repository pages to TOGAF ADM phases without forcing unnecessary artifacts.

Use this page for:
- ADM phase coverage
- missing artifacts
- tailoring decisions
- links to source pages

Avoid:
- claiming full TOGAF compliance without evidence
- turning this page into project status tracking
-->

## ADM Coverage

Formal TOGAF deliverables are mapped in [TOGAF Deliverable Coverage](architecture/artifact-register.md#togaf-deliverable-coverage). This template encourages coverage and traceability over duplicate documents.

| ADM Phase | Repository Pages | Status | Notes |
| --- | --- | --- | --- |
| Preliminary | [Principles](architecture/principles.md), [Governance](architecture/governance/README.md), [Artifact Register](architecture/artifact-register.md) | Planned | Record architecture principles, governance model, repository rules, artifact lifecycle, and status/version tracking. |
| A. Architecture Vision | [Architecture Vision](architecture/architecture-vision.md), [Stakeholders and Concerns](architecture/stakeholders-and-concerns.md) | Planned | Explain scope, stakeholders, value, constraints, and target outcome. |
| B. Business Architecture | [Business Architecture](architecture/business/README.md) | Planned | Capabilities, value streams, actors, processes, and policies. |
| C. Information Systems Architecture | [Information Systems](architecture/information-systems/README.md) | Planned | Application, data, service, API, and event architecture. |
| D. Technology Architecture | [Technology](architecture/technology/README.md) | Planned | Runtime, deployment, observability, and technology platform. |
| E. Opportunities And Solutions | [Architecture States](architecture/architecture-states/README.md), [Gap Analysis](architecture/architecture-states/gap-analysis.md), [Roadmap](architecture/implementation-migration/roadmap.md), [Transition Architectures](architecture/architecture-states/transition-architectures.md) | Planned | Compare baseline and target, identify gaps, and define candidate solution increments. |
| F. Migration Planning | [Work Packages](architecture/implementation-migration/work-packages.md), [Architecture Version Register](architecture/architecture-states/architecture-version-register.md) | Planned | Group delivery work into implementable packages and tie work to named architecture versions. |
| G. Implementation Governance | [Architecture Review](architecture/governance/architecture-review.md), [Readiness](architecture/implementation-migration/readiness.md) | Planned | Define review gates and architecture compliance evidence. |
| H. Architecture Change Management | [Change Control](architecture/governance/change-control.md), [Waivers](architecture/governance/waivers.md) | Planned | Govern changes, exceptions, and lifecycle updates. |
| Requirements Management | [Requirements](architecture/requirements.md) | Planned | Maintain central architecture-significant requirements continuously across all ADM phases; phase artifacts interpret and evidence them. |

## Tailoring Decisions

Record which TOGAF artifacts are intentionally omitted or simplified, and why.

## Validation Gate Pattern

Each ADM phase can move from `Draft` to `Approved` or `Baselined` when:

- stakeholder concerns are addressed;
- assumptions and open questions are listed;
- security, privacy, and operational impact are considered;
- affected decisions are recorded;
- baseline-to-target gaps are linked where relevant;
- the accountable owner or Architecture Board accepts the artifact.
