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

Describe what the architecture repository covers and which systems, products, organizations, or domains are in scope.

## Architecture Areas

| Area | Purpose |
| --- | --- |
| Architecture Vision | Why the architecture exists and what outcome it supports. |
| Glossary | Shared architecture and domain language used across artifacts. |
| Constraints | Solution limits that shape architecture options. |
| Business Architecture | Capabilities, value streams, actors, processes, and policies. |
| Information Systems Architecture | Applications, data, services, APIs, and integrations. |
| Technology Architecture | Runtime platform, deployment, operations, and approved technology standards. |
| Security Architecture | Security, privacy, controls, risks, and gaps. |
| Architecture States | Baseline, target, transition, version register, gap analysis, and risk register. |
| Implementation And Migration | Roadmap, transition architectures, work packages, and readiness. |
| Governance | Review, architecture contract, change control, waivers, and decision process. |
| Views And Diagrams | Stakeholder-specific viewpoints and diagram catalog. |

## Repository Rules

- Record durable decisions explicitly.
- Keep architecture content reviewed through pull requests.
- Link related artifacts instead of copying content.
- Keep current-state evidence distinct from target architecture.
- Mark assumptions and open questions clearly.
- Keep shared terms in the [Glossary](architecture/glossary.md).
- Track constraints separately from requirements in [Constraints](architecture/constraints.md).
- Track page-level status/version in the [Artifact Register](architecture/artifact-register.md).
- Track named baseline and target snapshots in [Architecture States](architecture/architecture-states/README.md).
