# Integrations And Events

<!--
Purpose:
Describe integrations, event contracts, source/consumer responsibilities, and reliability expectations.
-->

| Integration / Event | Producer | Consumers | Purpose | Reliability Notes |
| --- | --- | --- | --- | --- |
| ContextActivated | Identity / Access Service | Core Domain, Reporting, Audit | Announce that a user, organization, or operating context is ready for use. | Idempotent by event ID; consumers must tolerate duplicate delivery. |
| DomainCommandAccepted | Core Domain Service | Read Model / Reporting, Notification, Audit | Project operational state and notify interested actors. | At-least-once delivery; projection writes must be idempotent. |
| DomainOutcomeChanged | Core Domain Service | Read Model / Reporting, Notification, Audit | Keep read models, notifications, and evidence aligned with lifecycle changes. | Preserve event order per aggregate where required; retries must not duplicate side effects. |

## Integration Rules

- Record the producer and consumers for every architecture-significant event.
- Record idempotency, ordering, retry, replay, and dead-letter expectations.
- Link to API contracts or source definitions where available.

## Related Views

| View | Use When | Example |
| --- | --- | --- |
| Application Cooperation View | A reader needs to see which components publish, consume, serve, or depend on integration behavior. | [Application Cooperation Diagram](/architecture/information-systems/application-architecture?id=example-application-cooperation-diagram) |
| Data Flow View | A reader needs to see exchanged data, events, APIs, files, or external integration flows. | [Data Flow Diagram](/architecture/information-systems/data-architecture?id=example-data-flow-diagram) |
