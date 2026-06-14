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
