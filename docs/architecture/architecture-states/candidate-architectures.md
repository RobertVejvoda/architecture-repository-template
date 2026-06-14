# Candidate Architectures

<!--
Purpose:
Capture architecture options and early solution shapes before they are validated as target or transition architecture.

Use this page for:
- high-level architecture ideas that need assessment
- competing target options
- possible transition approaches
- assumptions, risks, and open questions before board acceptance

Avoid:
- presenting candidates as approved target architecture
- duplicating the accepted target or transition architecture
- tracking implementation tasks
-->

Candidate architectures are useful when architecture thinking exists before assessment, board review, or evidence is complete.

A candidate is not the target architecture. It is assessment input. Once accepted, the selected option is promoted into [Target Architecture](/architecture/architecture-states/target-architecture.md) or [Transition Architectures](/architecture/architecture-states/transition-architectures.md). Rejected options can stay here as context or be summarized in [Architecture Decisions](/architecture/decisions.md).

## Purpose And Granularity

Use this page for architecture options that need comparison, evidence, or governance before they become target or transition architecture. A candidate sketch should show the option and its tradeoffs; detailed implementation spikes and tasks belong in the delivery tool and should link back only when they provide evidence.

## Candidate Register

| Candidate ID | Candidate | Scope | Main Assumptions | Benefits | Risks / Gaps | Status | Outcome / Route |
| --- | --- | --- | --- | --- | --- | --- | --- |
| CAND-001 | Example candidate option. | Replace with the business functions, systems, data, integrations, operations, or governance scope covered. | Replace with assumptions that must be true for this candidate to work. | Replace with why this candidate may be useful. | Replace with missing evidence, concerns, or open questions. | Draft | Assess before promoting to target or transition architecture. |

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Candidate Architecture View | A reader needs to understand an unapproved option before assessment or selection. | [Candidate Architecture Sketch](#example-candidate-architecture-sketch) |
| Target Architecture View | A reader needs to compare a candidate with the accepted target direction. | [Target Architecture Overview](/architecture/architecture-states/target-architecture?id=example-target-architecture-overview) |

## Example Candidate Architecture Sketch

```plantuml
@startuml
!include <archimate/Archimate>
LAYOUT_TOP_DOWN()

Application_Component(app, "Mobile / Web App")
Application_Component(booking, "Booking Service")
Application_DataObject(bookingStore, "Booking Store")
Application_Component(eventBus, "Event Bus")
Application_Component(allocationWorker, "Allocation Worker")
Application_Component(readModel, "Reporting Read Model")
Technology_Node(managedRuntime, "Managed Runtime")
Technology_Node(managedDatabase, "Managed Database")
Motivation_Assessment(candidateRisk, "Operational Complexity Tradeoff")
Motivation_Requirement(req, "Restart-Safe State")

Rel_Flow(app, booking, "commands")
Rel_Access_rw(booking, bookingStore, "persists")
Rel_Triggering(booking, eventBus, "publishes")
Rel_Triggering(eventBus, allocationWorker, "triggers")
Rel_Triggering(eventBus, readModel, "projects")
Rel_Assignment(managedRuntime, booking, "hosts")
Rel_Assignment(managedRuntime, allocationWorker, "hosts")
Rel_Assignment(managedDatabase, bookingStore, "stores")
Rel_Association(req, bookingStore, "drives")
Rel_Association(candidateRisk, eventBus, "tradeoff")

' Layering hint: motivation above application above technology.
req -[hidden]down- app
candidateRisk -[hidden]down- eventBus
app -[hidden]down- managedRuntime
bookingStore -[hidden]down- managedDatabase
@enduml
```

## Status Values

| Status | Meaning |
| --- | --- |
| Draft | Candidate is being shaped and is not ready for review. |
| Assessment Input | Candidate is ready to compare against alternatives or assessment evidence. |
| Recommended | Candidate is recommended but not yet accepted by the Architecture Board or accountable owner. |
| Promoted | Candidate has been accepted and moved into target or transition architecture. |
| Rejected | Candidate was considered and not selected. |
| Superseded | Candidate was replaced by another candidate. |

## Candidate Record

Use this lightweight shape when a candidate needs more than one row:

| Field | Description |
| --- | --- |
| Candidate ID | Stable ID, for example `CAND-001`. |
| Scope | Business functions, systems, data, integrations, operations, or governance scope covered. |
| Architecture Sketch | Short narrative or diagram link. |
| Assumptions | What must be true for this candidate to work. |
| Benefits | Why this candidate may be useful. |
| Risks / Gaps | Known concerns, missing evidence, or unresolved questions. |
| Impacted Artifacts | Requirements, target, transition, data, application, technology, security, migration, governance, views. |
| Status | Draft, Assessment Input, Recommended, Promoted, Rejected, or Superseded. |
| Outcome / Route | Target architecture, transition architecture, decision, gap, risk, waiver, change set, or no further action. |

## Promotion Rule

Do not update [Target Architecture](/architecture/architecture-states/target-architecture.md) or [Transition Architectures](/architecture/architecture-states/transition-architectures.md) just because a candidate exists.

Promote a candidate only when it is accepted or explicitly selected for review. At that point:

1. Record or update the durable decision in [Architecture Decisions](/architecture/decisions.md) if alternatives were considered.
2. Use an [Architecture Change Set](/architecture/governance/architecture-change-set.md) when the selected candidate changes requirements, gaps, target, transition, domain architecture, migration, governance, or diagrams.
3. Update [Architecture Version Register](/architecture/architecture-states/architecture-version-register.md) only if the accepted candidate changes a named baseline, target, or transition snapshot.
4. Leave rejected or superseded candidates here with a short outcome so the reasoning is not lost.
