# Transition Architectures

<!--
Purpose:
Describe intermediate architecture states between baseline and target.

Use this page for:
- migration increments
- release architecture states
- dependency sequencing
- transition risks

Avoid:
- detailed sprint plans
- transitions that do not change architecture capability
-->

| Transition | From Version | To Version | Capabilities Added | Risks | Exit Criteria |
| --- | --- | --- | --- | --- | --- |
| T1 | Current State v0.1 | Foundation Target v0.1 | Architecture repository, principles, requirements, governance, and baseline evidence. | Stakeholder assumptions may remain incomplete. | Artifact register and initial decision log reviewed. |
| T2 | Foundation Target v0.1 | Pilot Target v0.1 | Durable state, protected ingress, readiness checks, and first operational views. | Accepted limitations must be explicit and time-bound. | Critical gaps closed or waived with linked evidence. |
| T3 | Pilot Target v0.1 | Production Target v0.1 | Restore drills, observability, operational runbooks, and conformance evidence. | Operational process may become too heavy if not pruned. | Architecture Board accepts readiness and residual risk. |

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Transition State View | A reader needs to see the baseline-to-target transition sequence. | [Transition State Timeline](#example-transition-state-timeline) |
| Roadmap View | A reader needs to see transition timing assumptions and milestone gates. | [Roadmap Gantt Chart](/architecture/implementation-migration/roadmap?id=example-roadmap-gantt-chart) |

## Example Transition State Timeline

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_LEFT_RIGHT()

Implementation_Plateau(current, "Current State v0.1")
Implementation_Plateau(foundation, "Foundation Target v0.1")
Implementation_Plateau(pilot, "Pilot Target v0.1")
Implementation_Plateau(production, "Production Target v0.1")
Implementation_WorkPackage(wp1, "WP-001\nArchitecture Foundation")
Implementation_WorkPackage(wp2, "WP-002\nPilot Readiness")
Implementation_WorkPackage(wp3, "WP-003\nRead Model Foundation")

Rel_Triggering(current, foundation, "T1")
Rel_Triggering(foundation, pilot, "T2")
Rel_Triggering(pilot, production, "T3")
Rel_Realization(wp1, foundation, "realizes")
Rel_Realization(wp2, pilot, "realizes")
Rel_Realization(wp3, pilot, "supports")
@enduml
```
