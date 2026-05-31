# Information Systems Architecture

<!--
Purpose:
Describe application and data architecture for systems that support the business architecture.

Use this page for:
- application and data architecture overview
- service and integration boundaries
- links to APIs, events, and data models

Avoid:
- cloud provider deployment specifics
- detailed operational runbooks
-->

## Contents

- [Application Architecture](architecture/information-systems/application-architecture.md)
- [Data Architecture](architecture/information-systems/data-architecture.md)
- [Integrations and Events](architecture/information-systems/integrations-events.md)
- [Service Catalog](architecture/information-systems/service-catalog.md)
- [API Contracts](architecture/information-systems/api-contracts.md)

## Requirement Interpretation Example

Use this section to show how Information Systems Architecture interprets central requirements from [Requirements Management](architecture/requirements.md). Keep the central statement stable and record application/data/API/event consequences here.

| Requirement | Information Systems Interpretation | Evidence | Gap |
| --- | --- | --- | --- |
| AR-FS-001 | FairSpot example: APIs derive tenant/user from authenticated context; owning services store tenant-scoped data; events and read models carry tenant context safely. | Application Architecture, Data Architecture, API Contracts, Integrations and Events. | Prove read-model projection isolation. |
