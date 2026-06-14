# Deployment Profiles

<!--
Purpose:
Describe supported deployment shapes and how they differ.

Use this page for:
- local, test, staging, production, or customer-owned profiles
- ingress and network boundaries
- platform dependencies
- environment-specific responsibilities

Avoid:
- credentials
- step-by-step runbooks unless needed for architecture review
-->

| Profile | Purpose | Key Components | Responsibilities |
| --- | --- | --- | --- |
| Local Development | Developer workflow and automated validation. | Local services, local dependencies, test identity, lightweight observability. | Development team owns setup and reset scripts. |
| Hosted Pilot | Controlled customer or stakeholder evaluation. | Public ingress, managed identity, persistent stores, monitoring, backup evidence. | Product/operator owns readiness and support boundary. |
| Customer-Owned Production | Deployment into a customer-controlled environment. | Customer-approved ingress, identity, data stores, secrets, observability. | Shared responsibilities must be documented before handoff. |

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Deployment View | A reader needs to see runtime nodes, ingress, networks, stores, and platform components. | [Deployment Diagram](#example-deployment-diagram) |
| Security And Privacy View | A reader needs to see trust boundaries, ingress controls, or sensitive data zones. | [Security And Privacy Diagram](/architecture/security/security-architecture?id=example-security-and-privacy-diagram) |

## Example Deployment Diagram

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_LEFT_RIGHT()

Technology_Device(device, "User Device")
Technology_Service(ingress, "Protected Ingress / WAF")
Technology_Node(runtime, "Cloud Runtime")
Technology_Artifact(api, "FairSpot API Artifact")
Technology_Artifact(worker, "Allocation Worker Artifact")
Technology_Node(database, "Database Node")
Technology_SystemSoftware(broker, "Event Broker")
Technology_Service(observability, "Observability Service")

Rel_Flow(device, ingress, "HTTPS")
Rel_Serving(ingress, runtime, "routes")
Rel_Assignment(runtime, api, "hosts")
Rel_Assignment(runtime, worker, "hosts")
Rel_Flow(api, database, "reads/writes")
Rel_Flow(worker, broker, "publishes/subscribes")
Rel_Serving(observability, runtime, "monitors")
@enduml
```
