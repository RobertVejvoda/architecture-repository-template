# Information Systems Architecture

<!--
Purpose:
Describe application, data, service, API, event, and integration architecture.
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Target</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Phase C</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

## Contents

- [Application Architecture](/architecture/information-systems/application-architecture.md)
- [Data Architecture](/architecture/information-systems/data-architecture.md)
- [Integrations and Events](/architecture/information-systems/integrations-events.md)
- [Service Catalog](/architecture/information-systems/service-catalog.md)
- [API Contracts](/architecture/information-systems/api-contracts.md)

## Requirement Coverage

| Requirement | Information Systems Interpretation | Impacted Artifacts | Evidence / Gap |
| --- | --- | --- | --- |
| AR-001 | APIs derive actor and scope from trusted context; owning services store scoped data; events and read models carry scope safely. | Application Architecture, Data Architecture, API Contracts, Integrations and Events. | Prove read-model and integration scope boundaries. |
| AR-002 | Operational state has clear ownership, persistence, backup, restore, and rebuild expectations. | Data Architecture, Service Catalog, Integrations and Events. | Link restore and replay evidence. |
