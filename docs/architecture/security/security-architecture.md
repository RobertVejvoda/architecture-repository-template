# Security Architecture

<!--
Purpose:
Describe the target security model at architecture level.
-->

## Security Themes

- identity and authentication
- authorization and access scope
- privileged operations and audit
- ingress and network exposure
- service-to-service trust
- secrets and configuration
- sensitive data protection
- backup, restore, export, and support access
- monitoring, alerting, and incident response

## Target Security Direction

| Area | Target Direction | Evidence / Artifact |
| --- | --- | --- |
| Identity | Use trusted identity integration and derive actor context from authenticated requests. | API Contracts, Controls |
| Authorization | Enforce role and organizational scope at API and service boundaries. | Controls, Application Architecture |
| Audit | Capture privileged actions and architecture-significant business events. | Audit service/catalog, Controls |
| Ingress | Route public traffic through approved protected ingress profiles. | Deployment Profiles, Technology Standards |
| Secrets | Keep secrets out of code, logs, backups, and exported evidence. | Runtime Platform, Controls |
| Monitoring | Emit security-relevant telemetry and alert on important failures. | Observability, Readiness |

## Open Security Questions

Move board-level or acceptance-blocking questions to [Architecture Governance Log](/architecture/governance/architecture-governance-log.md). Record confirmed security gaps in [Security Gap Register](/architecture/security/gap-register.md).

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Security And Privacy View | A reader needs to see trust boundaries, personal-data boundaries, controls, and material risks. | [Security And Privacy Diagram](#example-security-and-privacy-diagram) |
| Deployment View | A reader needs to see runtime, ingress, network, and platform boundaries that affect security. | [Deployment Diagram](/architecture/technology/deployment-profiles?id=example-deployment-diagram) |

## Example Security And Privacy Diagram

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_TOP_DOWN()

Technology_Device(user, "User Device")
Technology_Service(edge, "TLS + WAF + Auth")
Application_Component(api, "FairSpot API")
Motivation_Requirement(authz, "Role / Scope Authorization")
Application_DataObject(scopeData, "Booking / User Scope Data")
Application_DataObject(audit, "Audit Events")
Motivation_Constraint(retention, "Retention Policy")
Motivation_Assessment(risk, "Missing Projection Isolation Evidence")

Rel_Flow(user, edge, "flow")
Rel_Serving(edge, api, "serves")
Rel_Association(authz, api, "constrains")
Rel_Access_rw(api, scopeData, "accesses")
Rel_Access_w(api, audit, "creates")
Rel_Association(retention, scopeData, "constrains")
Rel_Association(risk, scopeData, "risk")

' Layering hint: requirements above application/data above technology.
authz -[hidden]down- api
retention -[hidden]down- scopeData
risk -[hidden]down- audit
api -[hidden]down- edge
scopeData -[hidden]down- user
@enduml
```
