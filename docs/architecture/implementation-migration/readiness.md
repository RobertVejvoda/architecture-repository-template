# Readiness

<!--
Purpose:
Track architecture readiness before pilot, production, migration, or release acceptance.
-->

| Readiness Area | Expectation | Status | Evidence / Notes |
| --- | --- | --- | --- |
| Architecture Readiness | Required artifacts are drafted, reviewed, and gaps/risks are visible. | Planned | Link artifact register and version register. |
| Data Readiness | Authoritative stores, retention, scope boundaries, migration, and rebuild strategy validated. | Planned | Link data architecture and gap analysis. |
| Security Readiness | Identity, authorization, secrets, ingress, audit, and privacy controls validated. | Planned | Link controls, security gap register, and waivers. |
| Operational Readiness | Monitoring, alerting, backup, restore, runbooks, and support ownership are accepted. | Planned | Link observability, deployment profile, and restore evidence. |
| Delivery Readiness | Work packages, dependencies, handover, and acceptance evidence are clear. | Planned | Link roadmap, work packages, and architecture contract. |

## Readiness Rules

- Do not mark an area ready without evidence or explicit risk acceptance.
- Link evidence instead of copying long test logs or delivery notes.
- Record unresolved readiness issues as gaps, risks, waivers, or governance log items.

## Purpose And Granularity

Use this page to show whether the architecture is ready for a pilot, production release, migration step, or customer handoff. Keep evidence links here; keep detailed test logs, support procedures, incident tickets, and delivery task lists in their source systems.

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Readiness And Resilience View | A reader needs to see the readiness evidence path for health, alerting, restore, audit, support, and residual risk. | [Operational Readiness And Resilience View](#example-operational-readiness-and-resilience-view) |
| Roadmap View | A reader needs to see when readiness gates are expected. | [Roadmap Gantt Chart](/architecture/implementation-migration/roadmap?id=example-roadmap-gantt-chart) |

## Example Operational Readiness And Resilience View

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_TOP_DOWN()

Application_Component(fairspot, "FairSpot Runtime")
Technology_Service(health, "Health Checks")
Technology_Service(alerting, "Alerting")
Technology_Service(observability, "Logs / Metrics / Traces")
Technology_Service(backupRestore, "Backup / Restore")
Business_Process(incident, "Incident Response")
Business_Actor(operator, "Operator")
Application_DataObject(audit, "Audit Evidence")
Implementation_Deliverable(evidence, "Readiness Evidence")
Motivation_Requirement(state, "AR-002\nRestart-Safe State")
Motivation_Assessment(risk, "Accepted Residual Risk")

Rel_Serving(health, fairspot, "checks")
Rel_Serving(observability, fairspot, "observes")
Rel_Triggering(alerting, incident, "alerts")
Rel_Assignment(operator, incident, "owns")
Rel_Serving(backupRestore, fairspot, "recovers")
Rel_Access_w(fairspot, audit, "creates")
Rel_Realization(evidence, state, "proves")
Rel_Association(incident, evidence, "updates")
Rel_Association(risk, evidence, "if incomplete")

' Layering hint: business operation above application/evidence above technology.
operator -[hidden]down- fairspot
incident -[hidden]down- evidence
fairspot -[hidden]down- health
audit -[hidden]down- backupRestore
@enduml
```
