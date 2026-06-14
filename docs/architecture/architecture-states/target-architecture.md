# Target Architecture

<!--
Purpose:
Describe the intended future architecture for a named version or scope.

Use this page for:
- target architecture summary
- business/application/data/technology/security target shape
- target assumptions and constraints
- acceptance criteria

Avoid:
- hiding unresolved gaps
- presenting unapproved ideas as baselined target architecture
-->

## Target Summary

Describe the intended target state.

## Purpose And Granularity

Use this page to describe the accepted or proposed future architecture state for a named scope or version. Keep it at architecture decision level: target capabilities, application/data/technology/security shape, constraints, and acceptance criteria. Delivery tasks and sprint sequencing belong in work packages and the delivery tool.

## Target Characteristics

| Area | Target State | Acceptance Criteria |
| --- | --- | --- |
| Business | Desired business capability/process state. | How fit is validated. |
| Applications | Desired application/service state. | How conformance is validated. |
| Data | Desired data ownership/lifecycle state. | How conformance is validated. |
| Technology | Desired runtime/deployment state. | How conformance is validated. |
| Security | Desired security/privacy state. | How conformance is validated. |

## Assumptions

Record assumptions that must be revisited before baselining.

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Target Architecture View | A reader needs a high-level accepted future-state picture across business, application, data, technology, and security concerns. | [Target Architecture Overview](#example-target-architecture-overview) |
| Transition State View | A reader needs to see how the architecture moves from baseline to target. | [Transition State Timeline](/architecture/architecture-states/transition-architectures?id=example-transition-state-timeline) |

## Example Target Architecture Overview

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_TOP_DOWN()

Business_Process(request, "Request Parking")
Application_Component(app, "Mobile / Web App")
Technology_Service(edge, "Protected Ingress")
Application_Component(booking, "Booking Service")
Application_Component(allocation, "Allocation Service")
Application_Component(readModel, "Reporting Read Model")
Application_Component(notification, "Notification Service")
Application_Component(audit, "Audit Service")
Application_DataObject(bookingData, "Booking Data")
Application_DataObject(projectionData, "Projection Data")
Application_Event(events, "Domain Events")
Technology_Service(observability, "Observability")
Motivation_Requirement(security, "Scoped Access And Audit")

Rel_Serving(app, request, "supports")
Rel_Flow(app, edge, "HTTPS")
Rel_Serving(edge, booking, "routes")
Rel_Access_rw(booking, bookingData, "owns")
Rel_Triggering(booking, events, "publishes")
Rel_Triggering(events, allocation, "triggers")
Rel_Triggering(events, readModel, "projects")
Rel_Access_rw(readModel, projectionData, "owns")
Rel_Triggering(allocation, notification, "notifies")
Rel_Triggering(booking, audit, "records")
Rel_Serving(observability, booking, "monitors")
Rel_Association(security, edge, "constrains")
Rel_Association(security, audit, "requires")

' Layering hint: business above application above technology.
security -[hidden]down- request
request -[hidden]down- app
request -[hidden]down- booking
app -[hidden]down- edge
booking -[hidden]down- observability
@enduml
```
