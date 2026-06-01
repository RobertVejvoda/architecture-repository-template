# Architecture Repository Template

This site is a reusable skeleton for a TOGAF 10-inspired architecture repository.

Use it to structure architecture content around stakeholder concerns, ADM phases, layered architecture views, decisions, governance, and implementation migration planning.

## Template Version

This page tracks the version of the template document structure itself. Project-specific baseline, target, and transition architecture versions should be tracked in [Architecture Version Register](architecture/architecture-states/architecture-version-register.md).

| Version | Date | Status | Summary | Migration Notes |
| --- | --- | --- | --- | --- |
| 0.9 | 2026-06-01 | Draft | Limited metadata tables to top-level Architecture Repository pages and the artifact register. | Track detailed child artifacts from the Artifact Register instead of repeating metadata on every page. |
| 0.8 | 2026-06-01 | Draft | Added standards catalog, glossary, constraints, risk register, and architecture contract. | Use these artifacts to make approved choices, shared language, solution limits, non-security risks, and delivery conformance explicit. |
| 0.7 | 2026-06-01 | Draft | Linked ADM checklist review gates to Architecture Review and Architecture Board governance. | Use the ADM checklist as the working readiness tool, Architecture Review as the review process, and Architecture Board as the decision owner. |
| 0.6 | 2026-05-31 | Draft | Replaced thin placeholder rows with three meaningful sample rows across architecture artifacts. | Template users should keep sample rows until they can replace them with project-specific content, then preserve at least three representative rows where the pattern is not obvious. |
| 0.5 | 2026-05-31 | Draft | Added artifact metadata to major architecture artifacts, an Architecture Board page, and FairSpot requirement-to-gap/work-package examples. | Repositories using the template should keep decisions in the decision log, define board governance separately, and trace requirements to phase impacts, gaps, and work packages. |
| 0.4 | 2026-05-31 | Draft | Added cross-phase Requirements Management guidance with a FairSpot-style example. | Requirements should be generic and centrally tracked, then interpreted by each affected ADM phase with evidence and gaps. |
| 0.3 | 2026-05-31 | Draft | Changed artifact metadata examples to compact metadata tables without visible headers. | Repositories using the template should prefer two-column metadata tables with bold field names and normal values. |
| 0.2 | 2026-05-31 | Draft | Added architecture states, artifact register, and TOGAF deliverable coverage mapping. | Repositories using the template should map formal deliverables to existing pages before creating standalone deliverable documents. |
| 0.1 | 2026-05-31 | Draft | Initial TOGAF-style architecture repository skeleton. | First usable baseline. |

## Reader Paths

| Reader | Start here | Purpose |
| --- | --- | --- |
| Sponsor or product owner | [Architecture Vision](architecture/architecture-vision.md) | Understand the target outcome and business context. |
| Architect | [Architecture Repository](architecture/README.md) and [ADM Map](architecture/togaf-adm-map.md) | Navigate architecture artifacts and ADM coverage. |
| Business stakeholder | [Business Architecture](architecture/business/README.md) | Understand capabilities, value streams, actors, processes, and policies. |
| Technical stakeholder | [Information Systems](architecture/information-systems/README.md) and [Technology](architecture/technology/README.md) | Understand applications, data, integrations, runtime, and deployment. |
| Security reviewer | [Security Architecture](architecture/security/README.md) | Understand security, privacy, controls, and known gaps. |
| Delivery lead | [Implementation And Migration](architecture/implementation-migration/README.md) | Understand roadmap, transition states, work packages, and readiness. |
| Architecture governor | [Architecture States](architecture/architecture-states/README.md) and [Artifact Register](architecture/artifact-register.md) | Understand baseline/target versions, artifact status, and gaps. |
| Implementation team | [Technology Standards](architecture/technology/standards.md) and [Architecture Contract](architecture/governance/architecture-contract.md) | Understand approved choices and conformance expectations. |

## How To Use This Template

- Keep each page focused on one architecture concern.
- Prefer links over duplication.
- Record durable decisions explicitly.
- Keep diagrams indexed from one place.
- Separate target architecture from implementation evidence.
- Delete template guidance only after replacing it with project-specific content.
