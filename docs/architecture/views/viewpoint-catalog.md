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
| Business Capability View | Sponsor, business owner, architect | Which business capabilities are in scope and how mature or critical are they? | Business Architecture, Capabilities |
| Application Cooperation View | Architect, delivery lead, integration owner | Which applications/services collaborate and where are the integration boundaries? | Application Architecture, Integrations and Events |
| Deployment And Operations View | Operator, security reviewer, architecture board | How is the solution deployed, secured, monitored, and recovered in each profile? | Technology Architecture, Deployment Profiles, Readiness |

## Viewpoint Groups

| Group | Architecture Area | Typical Questions |
| --- | --- | --- |
| Business and Functional Architecture | [Business Architecture](/architecture/business/) | What does the organization do, which functions/capabilities are in scope, and how are products/services realized? |
| Information and Data Architecture | [Information Systems Architecture](/architecture/information-systems/) | What information exists, who owns it, how does it move, and how is it structured over its lifecycle? |
| Application Architecture | [Information Systems Architecture](/architecture/information-systems/) | Which applications support business processes/functions, and how do applications exchange data or serve use cases? |
| Technology Architecture | [Technology Architecture](/architecture/technology/) | Where does the solution run, which nodes/components are deployed, and what platform boundaries exist? |

## Detailed Viewpoint Catalog

| Viewpoint | Group | Audience | Concern Answered | Owning Artifact | Typical Diagram |
| --- | --- | --- | --- | --- | --- |
| Process Classification View | Business and Functional Architecture | Business owner, process owner, architect | Which processes exist and how are they grouped by management, core, and support responsibility? | [Business Processes](/architecture/business/business-processes) | Process Classification Diagram |
| Business Process View | Business and Functional Architecture | Process owner, operations lead, auditor | How does a business process flow across actors, decisions, events, and outcomes? | [Business Processes](/architecture/business/business-processes) | Business Process Diagram |
| Organized Process View | Business and Functional Architecture | Business owner, HR/operations lead | Which organizational units or roles perform each process step? | [Actors and Roles](/architecture/business/actors-roles), [Business Processes](/architecture/business/business-processes) | Organized Process Diagram |
| Functional Architecture View | Business and Functional Architecture | Sponsor, product owner, architect | Which business functions/capabilities exist and how do they relate to product scope and application responsibility? | [Capabilities](/architecture/business/capabilities) | Functional Architecture Diagram |
| Organization View | Business and Functional Architecture | Business owner, governance reviewer | Which organizational units, roles, responsibilities, and reporting relationships matter to the architecture? | [Actors and Roles](/architecture/business/actors-roles), [Governance](/architecture/governance/) | Organization Model |
| Product and Service Catalog View | Business and Functional Architecture | Sponsor, product owner, customer evaluator | Which products, services, and service options are offered or deferred? | [Capabilities](/architecture/business/capabilities), [Architecture Vision](/architecture/architecture-vision) | Product and Service Catalog |
| Product and Service Realization View | Business and Functional Architecture | Product owner, architect | Which processes, functions, applications, and technology realize each product or service? | [Value Streams](/architecture/business/value-streams), [Application Architecture](/architecture/information-systems/application-architecture) | Product and Service Realization |
| Information Model View | Information and Data Architecture | Data owner, architect, integrator | Which business information concepts exist and how do they relate? | [Data Architecture](/architecture/information-systems/data-architecture) | Information Model |
| Information Lifecycle View | Information and Data Architecture | Data owner, security/privacy reviewer | How is information created, used, retained, archived, erased, or rebuilt? | [Data Architecture](/architecture/information-systems/data-architecture), [Privacy Architecture](/architecture/security/privacy-architecture) | Information Lifecycle Diagram |
| Application Data Model View | Information and Data Architecture | Data architect, implementer | Which application-owned data structures support each service or bounded context? | [Data Architecture](/architecture/information-systems/data-architecture), [Service Catalog](/architecture/information-systems/service-catalog) | Application Data Model |
| Application Data Dictionary View | Information and Data Architecture | Data owner, implementer, reviewer | What do important application data entities, attributes, and classifications mean? | [Data Architecture](/architecture/information-systems/data-architecture), [API Contracts](/architecture/information-systems/api-contracts) | Application Data Dictionary |
| Application Data Flow View | Information and Data Architecture | Data owner, security reviewer, integrator | Which data flows cross applications, events, APIs, files, or external integrations? | [Integrations and Events](/architecture/information-systems/integrations-events), [API Contracts](/architecture/information-systems/api-contracts) | Application Data Flows Catalog |
| Applications Over Business Process View | Application Architecture | Business owner, architect, implementer | Which applications support each business process step? | [Application Architecture](/architecture/information-systems/application-architecture), [Business Processes](/architecture/business/business-processes) | Applications mapped over Business Process |
| End-to-End Application Exchange View | Application Architecture | Architect, integration owner | How do applications exchange information across the full end-to-end flow? | [Integrations and Events](/architecture/information-systems/integrations-events) | End-to-end Application Exchange Diagram |
| Application Exchange View | Application Architecture | Architect, implementer, integrator | Which application-to-application interfaces, events, and APIs exist? | [Integrations and Events](/architecture/information-systems/integrations-events), [API Contracts](/architecture/information-systems/api-contracts) | Application Exchange Diagram |
| Applications Over Functional Architecture View | Application Architecture | Product owner, architect | Which applications realize which business functions/capabilities? | [Application Architecture](/architecture/information-systems/application-architecture), [Capabilities](/architecture/business/capabilities) | Applications mapped over Functional Architecture |
| Application Use-Case View | Application Architecture | Product owner, implementer, tester | Which users or systems use each application capability? | [Application Architecture](/architecture/information-systems/application-architecture), [Service Catalog](/architecture/information-systems/service-catalog) | Application Use-Case Diagram |
| Application Logical Architecture View | Application Architecture | Architect, implementer | What are the logical application components, services, dependencies, and responsibilities? | [Application Architecture](/architecture/information-systems/application-architecture), [Service Catalog](/architecture/information-systems/service-catalog) | Application Logical Architecture Diagram |
| Physical Application Architecture View | Application Architecture | Architect, operator | How do logical applications map to deployable units, processes, stores, and runtime boundaries? | [Runtime Platform](/architecture/technology/runtime-platform), [Deployment Profiles](/architecture/technology/deployment-profiles) | Physical Application Architecture Diagram |
| Deployment View | Technology Architecture | Operator, client IT, security reviewer | Which runtime nodes, networks, ingress points, stores, and platform components host the solution? | [Deployment Profiles](/architecture/technology/deployment-profiles), [Runtime Platform](/architecture/technology/runtime-platform) | Deployment Diagram |
