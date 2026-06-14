# Business Capabilities

<!--
Purpose:
Name stable business abilities needed by the architecture.
-->

| Capability | Description | Priority | Notes |
| --- | --- | --- | --- |
| Customer / User Management | Identify, onboard, and manage the people or organizations that use the solution. | High | Replace with project-specific capability names. |
| Core Domain Operation | Execute the main business outcome supported by the architecture. | High | Keep capability names stable and business-oriented. |
| Reporting And Insight | Provide approved operational, management, or compliance views. | Medium | Link to data ownership and reporting requirements. |
| Operations And Support | Run, monitor, support, recover, and improve the solution. | High | Link to technology, readiness, and governance artifacts. |

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Business Capability View | A reader needs to see in-scope capabilities, priorities, grouping, or maturity. | [Capability Map](#example-capability-map) |

## Example Capability Map

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_TOP_DOWN()

Strategy_Capability(fairspot, "FairSpot Parking Management")
Strategy_Capability(request, "Parking Request Management")
Strategy_Capability(eligibility, "Eligibility And Access Scope")
Strategy_Capability(allocation, "Fair Allocation / Lottery")
Strategy_Capability(cancellation, "Cancellation And Reallocation")
Strategy_Capability(notifications, "Notifications")
Strategy_Capability(reporting, "Operational Reporting")
Strategy_Capability(admin, "Administration And Audit")

Rel_Composition(fairspot, request)
Rel_Composition(fairspot, eligibility)
Rel_Composition(fairspot, allocation)
Rel_Composition(fairspot, cancellation)
Rel_Composition(fairspot, notifications)
Rel_Composition(fairspot, reporting)
Rel_Composition(fairspot, admin)
@enduml
```
