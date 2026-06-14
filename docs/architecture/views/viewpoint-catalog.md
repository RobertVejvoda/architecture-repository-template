# Viewpoint Catalog

<!--
Purpose:
Define which views exist, who they serve, and what concerns they answer.

Use this page for:
- viewpoint name
- audience
- concern answered
- source pages or diagrams

Avoid:
- diagrams without clear audience or purpose
- framework labels that do not help readers
-->

| Viewpoint | Audience | Concern Answered | Source |
| --- | --- | --- | --- |
| Solution Context View | Sponsor, architect, customer IT, security reviewer | What is inside the architecture scope and which external actors or services influence it? | [Architecture Vision](/architecture/architecture-vision), [Target Architecture](/architecture/architecture-states/target-architecture) |
| Requirement Traceability View | Architecture owner, architecture board, delivery lead | How do concerns trace to requirements, decisions, gaps, work packages, and evidence? | [Requirements](/architecture/requirements), [Decisions](/architecture/decisions), [Gap Analysis](/architecture/architecture-states/gap-analysis), [Work Packages](/architecture/implementation-migration/work-packages) |
| Value Stream View | Sponsor, business owner, product owner | How does business value move from trigger to outcome? | [Value Streams](/architecture/business/value-streams), [Capabilities](/architecture/business/capabilities) |
| Business Capability View | Sponsor, business owner, architect | Which business capabilities are in scope and how mature or critical are they? | [Business Architecture](/architecture/business/), [Capabilities](/architecture/business/capabilities) |
| Business Process View | Process owner, operations lead, auditor | How does an important business process flow across actors, decisions, events, and outcomes? | [Business Processes](/architecture/business/business-processes), [Actors and Roles](/architecture/business/actors-roles) |
| Baseline Architecture View | Architect, architecture board, delivery lead | What current-state evidence is the target and gap analysis comparing against? | [Baseline Architecture](/architecture/architecture-states/baseline-architecture), [Gap Analysis](/architecture/architecture-states/gap-analysis) |
| Candidate Architecture View | Architect, architecture board, product owner | Which unapproved options are being assessed before target or transition selection? | [Candidate Architectures](/architecture/architecture-states/candidate-architectures), [Architecture Decisions](/architecture/decisions) |
| Target Architecture View | Sponsor, architect, delivery lead, architecture board | What future architecture state is accepted or proposed for the named scope? | [Target Architecture](/architecture/architecture-states/target-architecture), [Architecture Version Register](/architecture/architecture-states/architecture-version-register) |
| Application Cooperation View | Architect, delivery lead, integration owner | Which applications/services collaborate and where are the integration boundaries? | [Application Architecture](/architecture/information-systems/application-architecture), [Integrations and Events](/architecture/information-systems/integrations-events) |
| Data Flow View | Data owner, security reviewer, integrator | Which data flows cross applications, events, APIs, files, or external integrations? | [Data Architecture](/architecture/information-systems/data-architecture), [Integrations and Events](/architecture/information-systems/integrations-events) |
| Domain Lifecycle View | Business owner, data owner, architect, implementer | What states can an important business object pass through and which transitions are valid? | [Data Architecture](/architecture/information-systems/data-architecture), [Business Processes](/architecture/business/business-processes) |
| Deployment View | Operator, security reviewer, architecture board | Where does the solution run, and what platform, network, ingress, store, and observability boundaries exist? | [Technology Architecture](/architecture/technology/), [Deployment Profiles](/architecture/technology/deployment-profiles) |
| Security And Privacy View | Security reviewer, privacy reviewer, architecture board | Which controls, personal-data boundaries, risks, and gaps matter for the architecture decision? | [Security Architecture](/architecture/security/), [Privacy Architecture](/architecture/security/privacy-architecture), [Controls](/architecture/security/controls) |
| Roadmap View | Sponsor, product owner, delivery lead, architect | What are the major architecture outcomes, sequence, milestones, and dependencies? | [Roadmap](/architecture/implementation-migration/roadmap), [Work Packages](/architecture/implementation-migration/work-packages) |
| Readiness And Resilience View | Operator, security reviewer, architecture board, support lead | Which readiness evidence proves health, alerting, restore, audit, support, and residual risk are acceptable? | [Readiness](/architecture/implementation-migration/readiness), [Observability](/architecture/technology/observability), [Deployment Profiles](/architecture/technology/deployment-profiles) |
| Work Package Dependency View | Delivery lead, architect, architecture board | Which architecture work packages depend on each other and what do they deliver? | [Work Packages](/architecture/implementation-migration/work-packages), [Gap Analysis](/architecture/architecture-states/gap-analysis) |
| Transition State View | Architect, architecture board, delivery lead | How does the architecture move from baseline through transition states to target? | [Transition Architectures](/architecture/architecture-states/transition-architectures), [Architecture Version Register](/architecture/architecture-states/architecture-version-register) |
| Gap Closure View | Architect, delivery lead, risk owner | Which gaps are closed by which work packages, and what remains accepted or open? | [Gap Analysis](/architecture/architecture-states/gap-analysis), [Work Packages](/architecture/implementation-migration/work-packages) |

## How To Use This Catalog

Use the catalog as a navigation aid, not as a mandatory list of diagrams.

Keep the starter viewpoint list and diagram register aligned. A diagram in [Diagrams](/architecture/views/diagrams) should point to a viewpoint in this catalog, and a new framework-named view should be added only when it answers a real stakeholder concern. Keep extra ideas in optional viewpoint examples until they are promoted.

| Step | Action | Example |
| --- | --- | --- |
| 1 | Start with a stakeholder question. | "Which capabilities are in scope?" |
| 2 | Pick the smallest viewpoint that answers it. | Business Capability View |
| 3 | Follow the source architecture content. | Capabilities |
| 4 | Open or create the matching diagram only if a visual view helps. | Capability Map |
| 5 | Track the diagram lifecycle in [Diagrams](/architecture/views/diagrams). | Version, status, source, export, supported architecture version. |

## Architecture Areas

| Group | Architecture Area | Typical Questions |
| --- | --- | --- |
| Business and Functional Architecture | [Business Architecture](/architecture/business/) | What does the organization do, which functions/capabilities are in scope, and how are products/services realized? |
| Architecture States | [Architecture States](/architecture/architecture-states/) | What exists now, what options are being considered, what target is accepted, and how are gaps tracked? |
| Information and Data Architecture | [Information Systems Architecture](/architecture/information-systems/) | What information exists, who owns it, how does it move, and how is it structured over its lifecycle? |
| Application Architecture | [Information Systems Architecture](/architecture/information-systems/) | Which applications support business processes/functions, and how do applications exchange data or serve use cases? |
| Technology Architecture | [Technology Architecture](/architecture/technology/) | Where does the solution run, which nodes/components are deployed, and what platform boundaries exist? |
| Implementation and Migration | [Implementation And Migration](/architecture/implementation-migration/) | How are transition states, work packages, gaps, readiness, and roadmap milestones sequenced? |

## Optional Viewpoint Examples

Add these only when a real stakeholder question needs them.

The `Typical Diagram` column is a suggested visual pattern, not a requirement to create one page per viewpoint. Reuse the common examples in the owning architecture pages where they fit. Create a new diagram register row only when the viewpoint is promoted for a real project concern and has its own source/export lifecycle.

| Viewpoint | Group | Audience | Concern Answered | Owning Artifact | Typical Diagram |
| --- | --- | --- | --- | --- | --- |
| Process Classification View | Business and Functional Architecture | Business owner, process owner, architect | Which processes exist and how are they grouped by management, core, and support responsibility? | [Business Processes](/architecture/business/business-processes) | Process Classification Diagram |
| Business Process View | Business and Functional Architecture | Process owner, operations lead, auditor | How does a business process flow across actors, decisions, events, and outcomes? | [Business Processes](/architecture/business/business-processes) | [Business Process Diagram](/architecture/business/business-processes?id=example-business-process-diagram) |
| Organized Process View | Business and Functional Architecture | Business owner, HR/operations lead | Which organizational units or roles perform each process step? | [Actors and Roles](/architecture/business/actors-roles), [Business Processes](/architecture/business/business-processes) | Organized Process Diagram; see [Business Process example](/architecture/business/business-processes?id=example-business-process-diagram) |
| Functional Architecture View | Business and Functional Architecture | Sponsor, product owner, architect | Which business functions/capabilities exist and how do they relate to product scope and application responsibility? | [Capabilities](/architecture/business/capabilities) | Functional Architecture Diagram; see [Capability Map example](/architecture/business/capabilities?id=example-capability-map) |
| Organization View | Business and Functional Architecture | Business owner, governance reviewer | Which organizational units, roles, responsibilities, and reporting relationships matter to the architecture? | [Actors and Roles](/architecture/business/actors-roles), [Governance](/architecture/governance/) | Organization Model |
| Product and Service Catalog View | Business and Functional Architecture | Sponsor, product owner, customer evaluator | Which products, services, and service options are offered or deferred? | [Capabilities](/architecture/business/capabilities), [Architecture Vision](/architecture/architecture-vision) | Product and Service Catalog |
| Product and Service Realization View | Business and Functional Architecture | Product owner, architect | Which processes, functions, applications, and technology realize each product or service? | [Value Streams](/architecture/business/value-streams), [Application Architecture](/architecture/information-systems/application-architecture) | Product and Service Realization; see [Capability Map example](/architecture/business/capabilities?id=example-capability-map) |
| Information Model View | Information and Data Architecture | Data owner, architect, integrator | Which business information concepts exist and how do they relate? | [Data Architecture](/architecture/information-systems/data-architecture) | Information Model |
| Information Lifecycle View | Information and Data Architecture | Data owner, security/privacy reviewer | How is information created, used, retained, archived, erased, or rebuilt? | [Data Architecture](/architecture/information-systems/data-architecture), [Privacy Architecture](/architecture/security/privacy-architecture) | Information Lifecycle Diagram |
| Application Data Model View | Information and Data Architecture | Data architect, implementer | Which application-owned data structures support each service or bounded context? | [Data Architecture](/architecture/information-systems/data-architecture), [Service Catalog](/architecture/information-systems/service-catalog) | Application Data Model |
| Application Data Dictionary View | Information and Data Architecture | Data owner, implementer, reviewer | What do important application data entities, attributes, and classifications mean? | [Data Architecture](/architecture/information-systems/data-architecture), [API Contracts](/architecture/information-systems/api-contracts) | Application Data Dictionary |
| Application Data Flow View | Information and Data Architecture | Data owner, security reviewer, integrator | Which data flows cross applications, events, APIs, files, or external integrations? | [Integrations and Events](/architecture/information-systems/integrations-events), [API Contracts](/architecture/information-systems/api-contracts) | [Data Flow Diagram](/architecture/information-systems/data-architecture?id=example-data-flow-diagram) |
| Applications Over Business Process View | Application Architecture | Business owner, architect, implementer | Which applications support each business process step? | [Application Architecture](/architecture/information-systems/application-architecture), [Business Processes](/architecture/business/business-processes) | Applications mapped over Business Process; see [Business Process example](/architecture/business/business-processes?id=example-business-process-diagram) |
| End-to-End Application Exchange View | Application Architecture | Architect, integration owner | How do applications exchange information across the full end-to-end flow? | [Integrations and Events](/architecture/information-systems/integrations-events) | End-to-end Application Exchange Diagram; see [Data Flow example](/architecture/information-systems/data-architecture?id=example-data-flow-diagram) |
| Application Exchange View | Application Architecture | Architect, implementer, integrator | Which application-to-application interfaces, events, and APIs exist? | [Integrations and Events](/architecture/information-systems/integrations-events), [API Contracts](/architecture/information-systems/api-contracts) | Application Exchange Diagram; see [Application Cooperation example](/architecture/information-systems/application-architecture?id=example-application-cooperation-diagram) |
| Applications Over Functional Architecture View | Application Architecture | Product owner, architect | Which applications realize which business functions/capabilities? | [Application Architecture](/architecture/information-systems/application-architecture), [Capabilities](/architecture/business/capabilities) | Applications mapped over Functional Architecture; see [Capability Map example](/architecture/business/capabilities?id=example-capability-map) |
| Application Use-Case View | Application Architecture | Product owner, implementer, tester | Which users or systems use each application capability? | [Application Architecture](/architecture/information-systems/application-architecture), [Service Catalog](/architecture/information-systems/service-catalog) | Application Use-Case Diagram |
| Application Logical Architecture View | Application Architecture | Architect, implementer | What are the logical application components, services, dependencies, and responsibilities? | [Application Architecture](/architecture/information-systems/application-architecture), [Service Catalog](/architecture/information-systems/service-catalog) | Application Logical Architecture Diagram; see [Application Cooperation example](/architecture/information-systems/application-architecture?id=example-application-cooperation-diagram) |
| Physical Application Architecture View | Application Architecture | Architect, operator | How do logical applications map to deployable units, processes, stores, and runtime boundaries? | [Runtime Platform](/architecture/technology/runtime-platform), [Deployment Profiles](/architecture/technology/deployment-profiles) | Physical Application Architecture Diagram; see [Deployment example](/architecture/technology/deployment-profiles?id=example-deployment-diagram) |
| Deployment View | Technology Architecture | Operator, client IT, security reviewer | Which runtime nodes, networks, ingress points, stores, and platform components host the solution? | [Deployment Profiles](/architecture/technology/deployment-profiles), [Runtime Platform](/architecture/technology/runtime-platform) | [Deployment Diagram](/architecture/technology/deployment-profiles?id=example-deployment-diagram) |
