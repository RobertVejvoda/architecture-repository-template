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

## Artifact Metadata Standard

Each major architecture artifact should start with a small metadata table.

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft / In Review / Approved / Baselined / Deprecated / Superseded</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Baseline / Target / Transition / Gap Analysis / Cross-cutting</td></tr>
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
| Architecture Vision | [Architecture Vision](./architecture-vision.md) | Phase A | Target | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Business Architecture | [Business Architecture](./business/README.md) | Phase B | Target | Draft | 0.1 | Business Owner | Architecture Board | - | - |
| Information Systems Architecture | [Information Systems](./information-systems/README.md) | Phase C | Target | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Technology Architecture | [Technology](./technology/README.md) | Phase D | Target | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Security Architecture | [Security](./security/README.md) | Cross-cutting | Target | Draft | 0.1 | Security Lead | Architecture Board | - | - |
| Architecture States | [Architecture States](./architecture-states/README.md) | Cross-ADM | Baseline / Target / Gap Analysis | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |

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
| Architecture Repository | [Architecture Repository](./README.md), [Artifact Register](./artifact-register.md), [Architecture States](./architecture-states/README.md) | Planned | Repository structure, artifact status, versions, and architecture states. |
| Architecture Principles | [Principles](./principles.md) | Planned | Record durable principles and constraints. |
| Architecture Governance Framework | [Governance](./governance/README.md), [Architecture Review](./governance/architecture-review.md), [Change Control](./governance/change-control.md), [Waivers](./governance/waivers.md) | Planned | Define roles, reviews, lifecycle, exceptions, and approval gates. |
| Request for Architecture Work | [Architecture Vision](./architecture-vision.md), [Requirements](./requirements.md), [Stakeholders and Concerns](./stakeholders-and-concerns.md) | Planned | Capture trigger, sponsor need, scope, constraints, and desired outcome. |
| Statement of Architecture Work | [Architecture Vision](./architecture-vision.md), [Governance](./governance/README.md), [Architecture States](./architecture-states/README.md), [Gap Analysis](./architecture-states/gap-analysis.md) | Planned | Capture agreed scope, approach, deliverables, acceptance gates, roles, and responsibilities. |
| Stakeholder Map and Concerns | [Stakeholders and Concerns](./stakeholders-and-concerns.md) | Planned | Identify stakeholders, concerns, viewpoints, and acceptance needs. |
| Communications Plan | [Governance](./governance/README.md), [Architecture Review](./governance/architecture-review.md), [Change Control](./governance/change-control.md) | Planned | Keep lightweight unless the organization needs a formal plan. |
| Architecture Vision | [Architecture Vision](./architecture-vision.md) | Planned | State target outcome, business value, scope boundaries, risks, and success measures. |
| Requirements Repository | [Requirements](./requirements.md) | Planned | Track central architecture-significant requirements and their impact across ADM phases, gaps, work packages, and evidence. |
| Business Architecture Definition | [Business Architecture](./business/README.md) | Planned | Capabilities, value streams, actors, processes, and policies. |
| Data Architecture Definition | [Data Architecture](./information-systems/data-architecture.md) | Planned | Data ownership, classification, lifecycle, stores, integrations, and reporting/read-model direction. |
| Application Architecture Definition | [Application Architecture](./information-systems/application-architecture.md), [Service Catalog](./information-systems/service-catalog.md), [API Contracts](./information-systems/api-contracts.md) | Planned | Applications, services, APIs, events, and integration responsibilities. |
| Technology Architecture Definition | [Technology Architecture](./technology/README.md) | Planned | Runtime, deployment, platform, observability, and operational technology. |
| Security Architecture Definition | [Security Architecture](./security/README.md), [Privacy Architecture](./security/privacy-architecture.md), [Controls](./security/controls.md), [Gap Register](./security/gap-register.md) | Planned | Security and privacy can be cross-cutting instead of a strict ADM phase. |
| Architecture Requirements Specification | [Requirements](./requirements.md), [Controls](./security/controls.md), [Business Policies](./business/policies.md), [API Contracts](./information-systems/api-contracts.md) | Planned | Keep central requirements generic; let phase artifacts define their specific business, application, data, technology, security, and governance interpretation. |
| Architecture Definition Document | [Business Architecture](./business/README.md), [Information Systems](./information-systems/README.md), [Technology Architecture](./technology/README.md), [Security Architecture](./security/README.md), [Views and Diagrams](./views/README.md) | Planned | Covered by layer pages rather than one monolithic document. |
| Architecture Roadmap | [Roadmap](./implementation-migration/roadmap.md), [Transition Architectures](./architecture-states/transition-architectures.md), [Gap Analysis](./architecture-states/gap-analysis.md) | Planned | Show increments, dependencies, and target state progression. |
| Opportunities and Solutions | [Gap Analysis](./architecture-states/gap-analysis.md), [Roadmap](./implementation-migration/roadmap.md), [Work Packages](./implementation-migration/work-packages.md) | Planned | Group gaps into candidate solution increments and work packages. |
| Migration Plan | [Work Packages](./implementation-migration/work-packages.md), [Transition Architectures](./architecture-states/transition-architectures.md), [Readiness](./implementation-migration/readiness.md) | Planned | Keep issue/project-tool backed where possible. |
| Implementation and Migration Plan | [Roadmap](./implementation-migration/roadmap.md), [Work Packages](./implementation-migration/work-packages.md), [Readiness](./implementation-migration/readiness.md) | Planned | Show sequencing, acceptance gates, and readiness evidence. |
| Architecture Contract | [Architecture Review](./governance/architecture-review.md), [Change Control](./governance/change-control.md), [Waivers](./governance/waivers.md) | Planned | Capture conformance expectations through review gates unless a formal contract is required. |
| Compliance Assessment | [Architecture Review](./governance/architecture-review.md), [Readiness](./implementation-migration/readiness.md), [Gap Register](./security/gap-register.md) | Planned | Record review evidence and unresolved gaps. |
| Architecture Change Request | [Change Control](./governance/change-control.md), [Waivers](./governance/waivers.md), [Decisions](./decisions.md) | Planned | Lightweight change records are enough until external governance requires more. |
| Architecture Version Register | [Architecture Version Register](./architecture-states/architecture-version-register.md) | Planned | Track named baseline, target, transition, and superseded versions. |
