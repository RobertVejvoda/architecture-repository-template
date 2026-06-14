# Architecture Version Register

<!--
Purpose:
Track named baseline, target, and transition architecture versions.

Use this page for:
- architecture snapshot names
- type and status
- scope
- date and owner
- relationship to artifacts and gaps

Avoid:
- replacing per-page artifact versions
- recording every small documentation edit
-->

An architecture version is a named snapshot. It identifies which artifacts were reviewed together as one baseline, target, or transition architecture state.

Page-level versions are local to each artifact. They do not need to match the named architecture version.

| Architecture Version | Type | Status | Date | Scope | Related Artifacts | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| Current State v0.1 | Baseline | Draft | YYYY-MM-DD | Current-state evidence. | [Baseline Architecture](/architecture/architecture-states/baseline-architecture.md) | Initial baseline placeholder. |
| Target State v0.1 | Target | Draft | YYYY-MM-DD | Future target architecture. | [Target Architecture](/architecture/architecture-states/target-architecture.md) | Initial target placeholder. |
| Target State v0.5 | Target | Example | YYYY-MM-DD | Example reviewed target snapshot. | Requirements v0.2; Target Architecture v0.2; Application Architecture v0.2; Data Architecture v0.1; Technology Architecture v0.1; Decisions v0.3 | Demonstrates that artifact versions can differ within one named architecture snapshot. |

## Status Rules

| Status | Meaning |
| --- | --- |
| Draft | Version is being prepared. |
| In Review | Version is ready for formal review. |
| Approved | Version is accepted for its scope. |
| Baselined | Version is the active baseline or target for governance. |
| Superseded | Version has been replaced by a newer version. |
| Example | Row demonstrates usage and should be replaced in a project repository. |

## Related Artifact Versions

When adding a named architecture version, list the artifacts and page versions that were reviewed together. This makes it clear that only some pages may have changed for a given snapshot.

Use [Architecture Change Set](/architecture/governance/architecture-change-set.md) when a new version is caused by a material change across several artifacts.
