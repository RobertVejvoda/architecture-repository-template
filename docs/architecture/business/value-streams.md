# Value Streams

<!--
Purpose:
Show how value flows from trigger to outcome.
-->

| Value Stream | Trigger | Outcome | Related Capabilities |
| --- | --- | --- | --- |
| Onboard Participant | A new person, organization, or context needs access to the solution. | Participant can use the approved capabilities. | Customer / User Management, Operations And Support |
| Complete Core Outcome | A user or system starts the main business process. | The business outcome is accepted, rejected, completed, or routed for exception handling. | Core Domain Operation, Reporting And Insight |
| Operate And Improve | Operating evidence, feedback, or risk requires attention. | Service quality, controls, and architecture evidence improve. | Operations And Support, Reporting And Insight |

## Purpose And Granularity

Use this page to show business outcomes and major value stages. Keep step-by-step workflow, decisions, exceptions, and automation detail in [Business Processes](/architecture/business/business-processes.md), [Application Architecture](/architecture/information-systems/application-architecture.md), or [Data Architecture](/architecture/information-systems/data-architecture.md).

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Value Stream View | A reader needs to see business value from trigger to outcome without process or implementation detail. | [Value Stream Map](#example-value-stream-map) |
| Business Capability View | A reader needs to see which capabilities support the value stream. | [Capability Map](/architecture/business/capabilities?id=example-capability-map) |

## Example Value Stream Map

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_LEFT_RIGHT()

Business_Actor(employee, "Employee")
Business_Event(need, "Needs Parking")
Business_Process(request, "Request Parking")
Business_Process(allocate, "Fair Allocation")
Business_Process(useSpace, "Use Parking Allocation")
Business_Process(exception, "Cancel / Reallocate")
Business_Object(outcome, "Accepted Parking Outcome")
Strategy_Capability(requestMgmt, "Parking Request Management")
Strategy_Capability(allocation, "Fair Allocation / Lottery")
Strategy_Capability(operations, "Operations And Support")

Rel_Triggering(employee, need, "creates need")
Rel_Triggering(need, request, "starts")
Rel_Triggering(request, allocate, "eligible request")
Rel_Triggering(allocate, useSpace, "allocation")
Rel_Triggering(useSpace, exception, "if changed")
Rel_Access_w(useSpace, outcome, "realizes")
Rel_Association(requestMgmt, request, "supports")
Rel_Association(allocation, allocate, "supports")
Rel_Association(operations, exception, "supports")
@enduml
```

## Guidance

Use value streams to explain business outcomes. Keep process detail in [Business Processes](/architecture/business/business-processes.md) and technical flow in the appropriate information systems or technology artifact.
