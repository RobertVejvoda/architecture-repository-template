# Business Processes

<!--
Purpose:
Describe important business processes at a level useful for architecture validation.
-->

| Process | Purpose | Owner | Related Value Stream | Notes |
| --- | --- | --- | --- | --- |
| Manage Participant Access | Create, update, suspend, or remove access for people or organizations. | Business Owner | Onboard Participant | Link identity, privacy, and audit controls. |
| Execute Core Domain Process | Complete the main business outcome from trigger to accepted result. | Business Owner | Complete Core Outcome | Replace with project-specific process names. |
| Handle Exception Or Support Case | Resolve a case that cannot complete through the normal path. | Operations Owner | Complete Core Outcome | Include escalation, audit, and notification needs. |
| Review Operating Evidence | Review service health, risk, control, and improvement evidence. | Operations Owner | Operate And Improve | Link to readiness and observability. |

## Process Rules

- Keep processes business-readable.
- Put detailed implementation contracts in Information Systems artifacts.
- Put control obligations in Requirements, Policies, Security, and Governance artifacts.

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Business Process View | A reader needs to see process flow across actors, events, decisions, and outcomes. | [Business Process Diagram](#example-business-process-diagram) |
| Application Cooperation View | A reader needs to see which application services support or automate process steps. | [Application Cooperation Diagram](/architecture/information-systems/application-architecture?id=example-application-cooperation-diagram) |

## Example Business Process Diagram

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_TOP_DOWN()

Business_Actor(employee, "Employee")
Business_Process(request, "Request Parking Space")
Business_Event(draw, "Scheduled Draw Event")
Business_Process(allocate, "Allocate Parking Space")
Business_Object(bookingRequest, "Booking Request")
Business_Object(allocationResult, "Allocation Result")
Application_Service(bookingService, "Parking Booking Service")

Rel_Triggering(employee, request, "triggers")
Rel_Access_rw(request, bookingRequest, "creates/updates")
Rel_Serving(bookingService, request, "serves")
Rel_Triggering(draw, allocate, "triggers")
Rel_Access_w(allocate, allocationResult, "creates")
Rel_Flow(allocationResult, employee, "notifies")

' Layering hint: business process above supporting application service.
request -[hidden]down- bookingService
allocate -[hidden]down- bookingService
@enduml
```
