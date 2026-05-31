# Architecture States

<!--
Purpose:
Describe how the repository handles baseline, target, transition, and gap analysis architecture states.

Use this page for:
- architecture versioning model
- baseline and target definitions
- transition architecture rules
- gap analysis and traceability

Avoid:
- pretending a complete baseline exists when only current-state evidence is available
- mixing implementation task status with architecture state
-->

Architecture state pages explain what exists now, what should exist, how the architecture will move between states, and which gaps must be closed.

## Architecture State Types

| State Type | Meaning | Typical Use |
| --- | --- | --- |
| Baseline | A named snapshot of current architecture or current-state evidence. | Transformation starting point, current estate, implemented product state. |
| Target | A named future architecture accepted or under review. | Product target, migration target, pilot target, production target. |
| Transition | An intermediate architecture state between baseline and target. | Migration increments, release stages, staged rollout. |
| Gap Analysis | Structured comparison between baseline and target. | Work package discovery, risk tracking, readiness planning. |

## Versioning Rules

- Use named architecture versions for baseline and target snapshots, such as `Current State v1.0` or `Pilot Target v1.0`.
- Use page-level versions for individual artifacts, such as `0.1`, `0.2`, and `1.0`.
- `1.0` means the artifact is first approved or baselined for its stated scope.
- Git history remains the detailed change log.
- Repository tags may be used for formal architecture baselines, such as `architecture-baseline-v1.0`.

## Contents

- [Baseline Architecture](./baseline-architecture)
- [Target Architecture](./target-architecture)
- [Transition Architectures](./transition-architectures)
- [Architecture Version Register](./architecture-version-register)
- [Gap Analysis](./gap-analysis)
