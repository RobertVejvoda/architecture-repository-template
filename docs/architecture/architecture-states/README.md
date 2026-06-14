# Architecture States

<!--
Purpose:
Describe how the repository handles baseline, candidate, target, transition, gap, risk, and version tracking.

Use this page for:
- architecture versioning model
- baseline and target definitions
- candidate architecture handling
- transition architecture rules
- gap analysis and traceability
- architecture risk tracking

Avoid:
- pretending a complete baseline exists when only current-state evidence is available
- mixing implementation task status with architecture state
-->

Architecture state pages explain what exists now, what might exist, what should exist, how the architecture will move between states, and which gaps or risks must be managed.

## Architecture State Types

| State Type | Meaning | Typical Use |
| --- | --- | --- |
| Baseline | A named snapshot of current architecture or current-state evidence. | Transformation starting point, current estate, implemented product state. |
| Candidate | A possible solution option that is not yet accepted as target or transition architecture. | Assessment input, alternative comparison, option shaping. |
| Target | A named future architecture accepted or under review. | Product target, migration target, pilot target, production target. |
| Transition | An intermediate architecture state between baseline and target. | Migration increments, release stages, staged rollout. |
| Gap Analysis | Structured comparison between baseline and target. | Work package discovery, risk tracking, readiness planning. |
| Risk | Uncertain event or condition that can affect architecture outcomes. | Residual risk review, mitigation ownership, acceptance decisions. |

## Versioning Rules

- Use named architecture versions for baseline, target, and transition snapshots, such as `Current State v1.0`, `Pilot Target v1.0`, or `Transition State T1`.
- Use page-level versions for individual artifacts, such as `0.1`, `0.2`, and `1.0`.
- Page versions do not need to match architecture snapshot versions.
- `1.0` means the artifact is first approved or baselined for its stated scope.
- Git history remains the detailed change log.
- Repository tags may be used for formal architecture baselines, such as `architecture-baseline-v1.0`.

## Contents

- [Baseline Architecture](/architecture/architecture-states/baseline-architecture.md)
- [Candidate Architectures](/architecture/architecture-states/candidate-architectures.md)
- [Target Architecture](/architecture/architecture-states/target-architecture.md)
- [Transition Architectures](/architecture/architecture-states/transition-architectures.md)
- [Architecture Version Register](/architecture/architecture-states/architecture-version-register.md)
- [Gap Analysis](/architecture/architecture-states/gap-analysis.md)
- [Risk Register](/architecture/architecture-states/risk-register.md)
