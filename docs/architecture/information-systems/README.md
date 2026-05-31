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

- [Application Architecture](./application-architecture.md)
- [Data Architecture](./data-architecture.md)
- [Integrations and Events](./integrations-events.md)
- [Service Catalog](./service-catalog.md)
- [API Contracts](./api-contracts.md)

## Requirement Interpretation Example

Use this section to show how Information Systems Architecture interprets central requirements from [Requirements Management](../requirements.md). Keep the central statement stable and record application/data/API/event consequences here.

| Requirement | Information Systems Interpretation | Evidence | Gap |
| --- | --- | --- | --- |
| AR-FS-001 | FairSpot example: APIs derive tenant/user from authenticated context; owning services store tenant-scoped data; events and read models carry tenant context safely. | Application Architecture, Data Architecture, API Contracts, Integrations and Events. | Prove read-model projection isolation. |
