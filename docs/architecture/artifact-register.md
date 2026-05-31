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

| Field | Value |
| --- | --- |
| Status | Draft / In Review / Approved / Baselined / Deprecated / Superseded |
| Version | 0.1 |
| Architecture State | Baseline / Target / Transition / Gap Analysis / Cross-cutting |
| Baseline Version | Current State v1.0 |
| Target Version | Target State v1.0 |
| ADM Phase | Phase A / B / C / D / E / F / G / H / Requirements Management |
| Responsible | Architecture Owner |
| Accountable | Architecture Board |
| Last Reviewed | YYYY-MM-DD |
| Next Review | YYYY-MM-DD or event-triggered |

## Register

| Artifact | Path | ADM Phase | Architecture State | Status | Version | Responsible | Accountable | Last Reviewed | Next Review |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Architecture Vision | [Architecture Vision](/architecture/architecture-vision) | Phase A | Target | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Business Architecture | [Business Architecture](/architecture/business/) | Phase B | Target | Draft | 0.1 | Business Owner | Architecture Board | - | - |
| Information Systems Architecture | [Information Systems](/architecture/information-systems/) | Phase C | Target | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Technology Architecture | [Technology](/architecture/technology/) | Phase D | Target | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |
| Security Architecture | [Security](/architecture/security/) | Cross-cutting | Target | Draft | 0.1 | Security Lead | Architecture Board | - | - |
| Architecture States | [Architecture States](/architecture/architecture-states/) | Cross-ADM | Baseline / Target / Gap Analysis | Draft | 0.1 | Architecture Owner | Architecture Board | - | - |

## Status Definitions

| Status | Meaning |
| --- | --- |
| Draft | Content is being prepared and should not be treated as accepted. |
| In Review | Content is ready for stakeholder or architecture board review. |
| Approved | Accountable owner accepts the artifact for its stated scope. |
| Baselined | Artifact is part of a named architecture baseline or target version. |
| Deprecated | Artifact is retained for history but should not guide new work. |
| Superseded | Artifact has been replaced by another artifact or version. |
