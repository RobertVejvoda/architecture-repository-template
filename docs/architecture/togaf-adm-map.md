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

| ADM Phase | Repository Pages | Status | Notes |
| --- | --- | --- | --- |
| Preliminary | [Principles](/architecture/principles), [Governance](/architecture/governance/), [Artifact Register](/architecture/artifact-register) | Planned | Record architecture principles, governance model, repository rules, artifact lifecycle, and status/version tracking. |
| A. Architecture Vision | [Architecture Vision](/architecture/architecture-vision), [Stakeholders and Concerns](/architecture/stakeholders-and-concerns) | Planned | Explain scope, stakeholders, value, constraints, and target outcome. |
| B. Business Architecture | [Business Architecture](/architecture/business/) | Planned | Capabilities, value streams, actors, processes, and policies. |
| C. Information Systems Architecture | [Information Systems](/architecture/information-systems/) | Planned | Application, data, service, API, and event architecture. |
| D. Technology Architecture | [Technology](/architecture/technology/) | Planned | Runtime, deployment, observability, and technology platform. |
| E. Opportunities And Solutions | [Architecture States](/architecture/architecture-states/), [Gap Analysis](/architecture/architecture-states/gap-analysis), [Roadmap](/architecture/implementation-migration/roadmap), [Transition Architectures](/architecture/architecture-states/transition-architectures) | Planned | Compare baseline and target, identify gaps, and define candidate solution increments. |
| F. Migration Planning | [Work Packages](/architecture/implementation-migration/work-packages), [Architecture Version Register](/architecture/architecture-states/architecture-version-register) | Planned | Group delivery work into implementable packages and tie work to named architecture versions. |
| G. Implementation Governance | [Architecture Review](/architecture/governance/architecture-review), [Readiness](/architecture/implementation-migration/readiness) | Planned | Define review gates and architecture compliance evidence. |
| H. Architecture Change Management | [Change Control](/architecture/governance/change-control), [Waivers](/architecture/governance/waivers) | Planned | Govern changes, exceptions, and lifecycle updates. |
| Requirements Management | [Requirements](/architecture/requirements) | Planned | Maintain architecture-significant requirements and traceability. |

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
