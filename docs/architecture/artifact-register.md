# Architecture Artifact Register

<!--
Purpose:
Provide one index of architecture artifacts, their version/status, ownership, and review state.

Use this page for:
- artifact status across the architecture repository
- page-level version tracking
- accountable owner and approver
- review cadence and next review date
- links to architecture states and ADM phases

Avoid:
- replacing Git history as the detailed change log
- tracking implementation tasks that belong in delivery tools
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Cross-cutting</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Cross-ADM</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

## Section Metadata Standard

Top-level pages inside the Architecture Repository should start with a small metadata table. Detailed child artifacts should usually stay focused on their content and be tracked from this register instead of repeating the metadata block on every page.

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft / In Review / Approved / Baselined / Deprecated / Superseded</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Baseline / Candidate / Target / Transition / Gap Analysis / Cross-cutting</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Baseline Version</strong></td><td style="border:none;padding:3px 0;">Current State v1.0</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Target Version</strong></td><td style="border:none;padding:3px 0;">Target State v1.0</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Phase A / B / C / D / E / F / G / H / Requirements Management</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">YYYY-MM-DD</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">YYYY-MM-DD or event-triggered</td></tr>
</table>

## Register

| Artifact | Path | ADM Phase | Architecture State | Status | Version | Responsible | Accountable | Last Reviewed | Next Review |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Architecture Repository | [Architecture Repository](/architecture/README.md) | Preliminary / Cross-ADM | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Architecture In Plain Words | [Architecture In Plain Words](/architecture/plain-language-introduction.md) | Cross-ADM | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Repository Changes | [Repository Changes](/architecture/repository-changes.md) | Cross-ADM | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Architecture Vision | [Architecture Vision](/architecture/architecture-vision.md) | Phase A | Target | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Business Architecture | [Business Architecture](/architecture/business/README.md) | Phase B | Target | Draft | 0.1 | Business Owner | Architecture Board | - | - |
| Information Systems Architecture | [Information Systems](/architecture/information-systems/README.md) | Phase C | Target | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Technology Architecture | [Technology](/architecture/technology/README.md) | Phase D | Target | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Security Architecture | [Security](/architecture/security/README.md) | Cross-cutting | Target | Draft | 0.1 | Security Lead | Architecture Board | - | - |
| Architecture States | [Architecture States](/architecture/architecture-states/README.md) | Cross-ADM | Baseline / Candidate / Target / Transition / Gap Analysis | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Candidate Architectures | [Candidate Architectures](/architecture/architecture-states/candidate-architectures.md) | Phase E | Candidate | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Views And Diagrams | [Views And Diagrams](/architecture/views/README.md) | Cross-ADM | Cross-cutting | Draft | 0.7 | Architecture Owner | Architecture Board | 2026-06-14 | - |
| Requirements Repository | [Requirements](/architecture/requirements.md) | Requirements Management | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Constraints | [Constraints](/architecture/constraints.md) | Preliminary / Phase A | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Glossary | [Glossary](/architecture/glossary.md) | Preliminary / Requirements Management | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Architecture Decisions | [Decisions](/architecture/decisions.md) | Preliminary / Phase H | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Governance | [Governance](/architecture/governance/README.md) | Preliminary / Phase G / Phase H | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Architecture Board | [Architecture Board](/architecture/governance/architecture-board.md) | Preliminary / Phase G / Phase H | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Architecture Governance Log | [Architecture Governance Log](/architecture/governance/architecture-governance-log.md) | Preliminary / Phase H | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Architecture Change Set | [Architecture Change Set](/architecture/governance/architecture-change-set.md) | Phase H | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Architecture Contract | [Architecture Contract](/architecture/governance/architecture-contract.md) | Phase G | Cross-cutting | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Implementation And Migration | [Implementation And Migration](/architecture/implementation-migration/README.md) | Phase E/F/G | Transition / Migration | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Architecture Increment Checklist | [Architecture Increment Checklist](/architecture/implementation-migration/vertical-slice-checklist.md) | Phase E/F/G | Transition / Migration | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |

## Status Definitions

| Status | Meaning |
| --- | --- |
| Draft | Content is being prepared and should not be treated as accepted. |
| In Review | Content is ready for stakeholder or architecture board review. |
| Approved | Accountable owner accepts the artifact for its stated scope. |
| Baselined | Artifact is part of a named architecture baseline or target version. |
| Deprecated | Artifact is retained for history but should not guide new work. |
| Superseded | Artifact has been replaced by another artifact or version. |

## TOGAF Deliverable Coverage

Do not create a separate page for every formal TOGAF deliverable by default. Use this matrix to show where the required content is covered. Create a standalone deliverable page only when the content has no natural home elsewhere or an external governance process requires the formal artifact.

| TOGAF Deliverable / Content Area | Repository Coverage | Coverage Status | Notes |
| --- | --- | --- | --- |
| Architecture Repository | [Architecture Repository](/architecture/README.md), [Artifact Register](/architecture/artifact-register.md), [Architecture States](/architecture/architecture-states/README.md) | Planned | Repository structure, artifact status, versions, and architecture states. |
| Architecture Principles | [Principles](/architecture/principles.md), [Constraints](/architecture/constraints.md) | Planned | Record durable principles and solution constraints separately. |
| Architecture Governance Framework | [Governance](/architecture/governance/README.md), [Architecture Board](/architecture/governance/architecture-board.md), [Architecture Governance Log](/architecture/governance/architecture-governance-log.md), [Architecture Review](/architecture/governance/architecture-review.md), [Architecture Contract](/architecture/governance/architecture-contract.md), [Architecture Change Set](/architecture/governance/architecture-change-set.md), [Change Control](/architecture/governance/change-control.md), [Waivers](/architecture/governance/waivers.md) | Planned | Define roles, active question routing, reviews, conformance expectations, lifecycle, exceptions, and approval gates. |
| Request for Architecture Work | [Architecture Vision](/architecture/architecture-vision.md), [Requirements](/architecture/requirements.md), [Constraints](/architecture/constraints.md), [Stakeholders and Concerns](/architecture/stakeholders-and-concerns.md) | Planned | Capture trigger, sponsor need, scope, constraints, and desired outcome. |
| Statement of Architecture Work | [Architecture Vision](/architecture/architecture-vision.md), [Governance](/architecture/governance/README.md), [Architecture States](/architecture/architecture-states/README.md), [Gap Analysis](/architecture/architecture-states/gap-analysis.md), [Risk Register](/architecture/architecture-states/risk-register.md) | Planned | Capture agreed scope, approach, deliverables, acceptance gates, roles, responsibilities, and material risks. |
| Stakeholder Map and Concerns | [Stakeholders and Concerns](/architecture/stakeholders-and-concerns.md) | Planned | Identify stakeholders, concerns, viewpoints, and acceptance needs. |
| Communications Plan | [Governance](/architecture/governance/README.md), [Architecture Review](/architecture/governance/architecture-review.md), [Change Control](/architecture/governance/change-control.md) | Planned | Keep lightweight unless the organization needs a formal plan. |
| Architecture Vision | [Architecture Vision](/architecture/architecture-vision.md), [Constraints](/architecture/constraints.md) | Planned | State target outcome, business value, scope boundaries, constraints, risks, and success measures. |
| Requirements Repository | [Requirements](/architecture/requirements.md), [Glossary](/architecture/glossary.md) | Planned | Track central architecture-significant requirements, shared terms, and their impact across ADM phases, gaps, work packages, and evidence. |
| Business Architecture Definition | [Business Architecture](/architecture/business/README.md) | Planned | Capabilities, value streams, actors, processes, and policies. |
| Data Architecture Definition | [Data Architecture](/architecture/information-systems/data-architecture.md) | Planned | Data ownership, classification, lifecycle, stores, integrations, and reporting/read-model direction. |
| Application Architecture Definition | [Application Architecture](/architecture/information-systems/application-architecture.md), [Service Catalog](/architecture/information-systems/service-catalog.md), [API Contracts](/architecture/information-systems/api-contracts.md) | Planned | Applications, services, APIs, events, and integration responsibilities. |
| Technology Architecture Definition | [Technology Architecture](/architecture/technology/README.md), [Technology Standards](/architecture/technology/standards.md) | Planned | Runtime, deployment, platform, observability, operational technology, and approved standards. |
| Security Architecture Definition | [Security Architecture](/architecture/security/README.md), [Privacy Architecture](/architecture/security/privacy-architecture.md), [Controls](/architecture/security/controls.md), [Gap Register](/architecture/security/gap-register.md) | Planned | Security and privacy can be cross-cutting instead of a strict ADM phase. |
| Architecture Requirements Specification | [Requirements](/architecture/requirements.md), [Controls](/architecture/security/controls.md), [Business Policies](/architecture/business/policies.md), [API Contracts](/architecture/information-systems/api-contracts.md) | Planned | Keep central requirements generic; let phase artifacts define their specific interpretation. |
| Architecture Definition Document | [Business Architecture](/architecture/business/README.md), [Information Systems](/architecture/information-systems/README.md), [Technology Architecture](/architecture/technology/README.md), [Security Architecture](/architecture/security/README.md), [Views and Diagrams](/architecture/views/README.md) | Planned | Covered by layer pages rather than one monolithic document. |
| Candidate Architecture | [Candidate Architectures](/architecture/architecture-states/candidate-architectures.md) | Planned | Keep unvalidated options visible before they become target or transition architecture. |
| Architecture Roadmap | [Roadmap](/architecture/implementation-migration/roadmap.md), [Transition Architectures](/architecture/architecture-states/transition-architectures.md), [Gap Analysis](/architecture/architecture-states/gap-analysis.md), [Risk Register](/architecture/architecture-states/risk-register.md) | Planned | Show increments, dependencies, risks, and target state progression. |
| Opportunities and Solutions | [Candidate Architectures](/architecture/architecture-states/candidate-architectures.md), [Gap Analysis](/architecture/architecture-states/gap-analysis.md), [Roadmap](/architecture/implementation-migration/roadmap.md), [Work Packages](/architecture/implementation-migration/work-packages.md) | Planned | Compare options and group gaps into candidate solution increments and work packages. |
| Migration Plan | [Work Packages](/architecture/implementation-migration/work-packages.md), [Transition Architectures](/architecture/architecture-states/transition-architectures.md), [Readiness](/architecture/implementation-migration/readiness.md) | Planned | Keep issue/project-tool backed where possible. |
| Implementation and Migration Plan | [Roadmap](/architecture/implementation-migration/roadmap.md), [Work Packages](/architecture/implementation-migration/work-packages.md), [Architecture Increment Checklist](/architecture/implementation-migration/vertical-slice-checklist.md), [Readiness](/architecture/implementation-migration/readiness.md) | Planned | Show sequencing, acceptance gates, and readiness evidence. |
| Architecture Contract | [Architecture Contract](/architecture/governance/architecture-contract.md), [Architecture Review](/architecture/governance/architecture-review.md), [Technology Standards](/architecture/technology/standards.md), [Change Control](/architecture/governance/change-control.md), [Waivers](/architecture/governance/waivers.md) | Planned | Capture conformance expectations through review gates unless a formal contract is required. |
| Compliance Assessment | [Architecture Review](/architecture/governance/architecture-review.md), [Architecture Contract](/architecture/governance/architecture-contract.md), [Readiness](/architecture/implementation-migration/readiness.md), [Gap Register](/architecture/security/gap-register.md), [Risk Register](/architecture/architecture-states/risk-register.md) | Planned | Record review evidence, conformance result, unresolved gaps, and residual risks. |
| Architecture Change Request | [Architecture Change Set](/architecture/governance/architecture-change-set.md), [Change Control](/architecture/governance/change-control.md), [Waivers](/architecture/governance/waivers.md), [Decisions](/architecture/decisions.md) | Planned | Lightweight change records are enough until external governance requires more. |
| Architecture Version Register | [Architecture Version Register](/architecture/architecture-states/architecture-version-register.md) | Planned | Track named baseline, target, transition, and superseded versions. |
