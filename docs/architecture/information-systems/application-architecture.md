# Application Architecture

<!--
Purpose:
Describe application and service responsibilities, ownership, and boundaries.
-->

| Application / Service | Responsibility | Domain / Context | Interfaces |
| --- | --- | --- | --- |
| Identity / Access Service | Owns authentication integration, actor context, and authorization inputs. | Identity and access | Auth callbacks, token claims, user/context APIs |
| Core Domain Service | Owns the main business commands, lifecycle state, and domain events. | Core domain | User APIs, operations APIs, domain events |
| Read Model / Reporting Service | Owns approved read views, projections, report definitions, and export boundaries. | Data and reporting | Query APIs, projection events, report APIs |
| Notification / Communication Service | Owns outbound communication templates, delivery requests, and notification evidence. | Communication | Notification API, delivery events |
| Audit Service | Owns audit event capture and reviewable evidence. | Audit and evidence | Audit event API, audit queries |

## Boundary Rules

- Each authoritative write model has one owner.
- Cross-service reads use APIs, events, or approved read models.
- Hidden database coupling must be recorded as a gap, decision, or waiver.

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Application Cooperation View | A reader needs to understand how application components, services, events, and read models collaborate. | [Application Cooperation Diagram](#example-application-cooperation-diagram) |
| Data Flow View | A reader needs to understand data movement across application boundaries. | [Data Flow Diagram](/architecture/information-systems/data-architecture?id=example-data-flow-diagram) |

## Example Application Cooperation Diagram

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_LEFT_RIGHT()

Application_Component(booking, "Booking Component")
Application_Service(access, "Access Control Service")
Application_DataObject(bookingData, "Booking Data")
Application_Event(bookingEvents, "Booking Events")
Application_Component(allocation, "Allocation Component")
Application_Service(inventory, "Parking Inventory Service")
Application_Event(allocationEvents, "Allocation Events")
Application_Component(reporting, "Reporting Component")
Application_Component(notification, "Notification Component")

Rel_Serving(access, booking, "serves")
Rel_Access_rw(booking, bookingData, "reads/writes")
Rel_Triggering(booking, bookingEvents, "publishes")
Rel_Triggering(bookingEvents, allocation, "triggers")
Rel_Serving(inventory, allocation, "serves")
Rel_Triggering(allocation, allocationEvents, "publishes")
Rel_Triggering(bookingEvents, reporting, "triggers")
Rel_Triggering(allocationEvents, notification, "triggers")
@enduml
```
