# Baseline Architecture

<!--
Purpose:
Describe the current architecture state or current-state evidence used as the comparison point for target architecture.

Use this page for:
- current business process/system landscape
- current implemented product state
- known current constraints
- current risks and assumptions
- links to evidence

Avoid:
- inventing a complete baseline when evidence is partial
- mixing target-state aspirations into current-state description
-->

## Baseline Summary

Describe the current state used for gap analysis.

## Purpose And Granularity

Use this page to record the current architecture state or evidence baseline that target and gap analysis compare against. It does not need to model every implemented detail; record confidence, known limits, and links to evidence when the baseline is partial.

## Current-State Evidence

| Area | Current State | Evidence | Confidence |
| --- | --- | --- | --- |
| Business | Current process or capability state. | Link to source. | High / Medium / Low |
| Applications | Current systems or implemented product state. | Link to source. | High / Medium / Low |
| Data | Current data ownership and persistence. | Link to source. | High / Medium / Low |
| Technology | Current runtime or deployment state. | Link to source. | High / Medium / Low |

## Known Baseline Limits

Record what is intentionally incomplete or unknown in the baseline.

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Baseline Architecture View | A reader needs a high-level current-state picture before comparing target, transition, or gap content. | [Baseline Architecture Overview](#example-baseline-architecture-overview) |
| Gap Closure View | A reader needs to see which baseline-to-target gaps must be closed. | [Gap Closure Map](/architecture/architecture-states/gap-analysis?id=example-gap-closure-map) |

## Example Baseline Architecture Overview

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_TOP_DOWN()

Business_Actor(employee, "Employee")
Business_Process(manualRequest, "Parking Request Handling")
Application_Component(app, "Mobile / Web App")
Application_Component(booking, "Booking Component")
Application_DataObject(transientState, "Transient / Partially Proven State")
Application_Component(reporting, "Manual Reporting")
Technology_Node(runtime, "Prototype Runtime")
Technology_Node(localStore, "Local / Unproven Store")
Motivation_Assessment(gap, "Durability And Restore Evidence Gap")

Rel_Triggering(employee, manualRequest, "requests")
Rel_Serving(app, manualRequest, "supports")
Rel_Flow(app, booking, "request")
Rel_Access_rw(booking, transientState, "reads/writes")
Rel_Assignment(runtime, booking, "hosts")
Rel_Assignment(runtime, reporting, "hosts")
Rel_Flow(booking, localStore, "stores")
Rel_Association(gap, transientState, "limits confidence")

' Layering hint: business above application above technology.
employee -[hidden]down- app
manualRequest -[hidden]down- booking
booking -[hidden]down- runtime
transientState -[hidden]down- localStore
@enduml
```
