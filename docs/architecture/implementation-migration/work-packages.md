# Work Packages

<!--
Purpose:
Group implementation work into architecture-relevant packages.

Use this page for:
- work package name
- architecture objective
- affected capabilities/components
- dependencies and validation

Avoid:
- detailed issue/task duplication
- owner assignment churn
-->

| Work Package | Objective | Affected Architecture | Validation |
| --- | --- | --- | --- |
| WP-001 Architecture Foundation | Establish repository structure, metadata, requirements, principles, and governance model. | Architecture Repository, Requirements, Governance, Artifact Register. | Metadata present, links valid, board/decision process reviewed. |
| WP-002 Pilot Readiness | Close high-priority persistence, security, and operations gaps for a controlled pilot. | Gap Analysis, Security, Technology, Readiness, Deployment Profiles. | Smoke tests, security review, restore evidence, accepted waivers. |
| WP-003 Read Model Foundation | Add event inbox, projection runtime, and first operational read models. | Information Systems, Data Architecture, Integrations and Events. | Idempotency tests, replay/retry evidence, projection health endpoint. |

## Work Package Rules

- Keep work packages architecture-relevant and coarse-grained.
- Track detailed tasks, assignees, and sprint progress in the delivery tool.
- Link work packages to requirements, gaps, risks, and readiness evidence.

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Work Package Dependency View | A reader needs to see sequencing and dependencies across architecture work packages. | [Work Package Dependency Diagram](#example-work-package-dependency-diagram) |
| Gap Closure View | A reader needs to see which gaps are closed by each work package. | [Gap Closure Map](/architecture/architecture-states/gap-analysis?id=example-gap-closure-map) |

## Example Work Package Dependency Diagram

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_LEFT_RIGHT()

Implementation_WorkPackage(wp1, "WP-001\nArchitecture Foundation")
Implementation_WorkPackage(wp2, "WP-002\nPilot Readiness")
Implementation_WorkPackage(wp3, "WP-003\nRead Model Foundation")
Implementation_Deliverable(repo, "Reviewed Architecture Repository")
Implementation_Deliverable(readiness, "Pilot Readiness Evidence")
Implementation_Gap(gap1, "GAP-001\nDurable State")
Implementation_Gap(gap3, "GAP-003\nSecurity Readiness")

Rel_Triggering(wp1, wp2, "enables")
Rel_Triggering(wp1, wp3, "enables")
Rel_Triggering(wp3, wp2, "projection evidence")
Rel_Realization(wp1, repo, "delivers")
Rel_Realization(wp2, readiness, "delivers")
Rel_Association(gap1, wp2, "closed by")
Rel_Association(gap3, wp2, "closed by")
@enduml
```
