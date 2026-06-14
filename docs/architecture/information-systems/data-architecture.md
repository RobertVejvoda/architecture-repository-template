# Data Architecture

<!--
Purpose:
Describe data ownership, classification, lifecycle, read models, and evidence needs.
-->

| Data Area | Owner | Classification | Lifecycle / Retention | Notes |
| --- | --- | --- | --- | --- |
| User and access context | Identity / Access Service | Confidential | Retained according to identity and audit requirements. | Use least privilege and scope-aware reads. |
| Core domain records | Core Domain Service | Confidential | Retained for operational, audit, and dispute windows. | Authoritative writes belong to the owning service. |
| Derived read models | Read Model / Reporting Service | Internal / Confidential | Rebuildable from source events or synchronized sources where possible. | Track freshness, lineage, and rebuild limits. |
| Audit evidence | Audit Service | Confidential / Restricted | Retained according to legal, security, and operational policy. | Prevent modification by normal operators. |

## Data Rules

- Name the authoritative owner for each important data area.
- Separate command/write data from derived read models.
- Record retention, privacy, export, and deletion expectations.
- Link gaps where persistence, restore, lineage, or freshness evidence is missing.

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Data Flow View | A reader needs to see how data crosses applications, events, APIs, files, or external integrations. | [Data Flow Diagram](#example-data-flow-diagram) |
| Security And Privacy View | A reader needs to see personal-data boundaries, controls, or sensitive data risks. | [Security And Privacy Diagram](/architecture/security/security-architecture?id=example-security-and-privacy-diagram) |

## Example Data Flow Diagram

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_LEFT_RIGHT()

Application_Component(app, "Mobile / Web App")
Application_Service(bookingService, "Booking Service")
Application_DataObject(bookingRequest, "Booking Request")
Application_Component(eventBus, "Event Bus")
Application_Service(allocationService, "Allocation Service")
Application_Component(reporting, "Reporting Read Model")
Application_Service(notificationService, "Notification Service")

Rel_Flow(app, bookingService, "booking request")
Rel_Access_w(bookingService, bookingRequest, "creates")
Rel_Flow(bookingService, eventBus, "BookingSubmitted event")
Rel_Triggering(eventBus, allocationService, "triggers")
Rel_Triggering(eventBus, reporting, "triggers")
Rel_Flow(allocationService, notificationService, "allocation result")
@enduml
```
