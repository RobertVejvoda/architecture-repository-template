# Integrations And Events

<!--
Purpose:
Describe system interactions, integration contracts, event flows, and reliability expectations.

Use this page for:
- synchronous integrations
- asynchronous events
- event ownership
- idempotency and ordering expectations
- external systems

Avoid:
- duplicating full API specs
- transport-specific details unless architecture-significant
-->

| Integration / Event | Producer | Consumer | Purpose | Reliability Notes |
| --- | --- | --- | --- | --- |
| TenantReady | Customer / Tenant Service | Operations, DataHub, Notification | Announce that a tenant passed readiness and can receive controlled traffic. | Idempotent by event ID; consumers must tolerate duplicate delivery. |
| RequestSubmitted | Booking / Allocation Service | DataHub, Notification, Audit | Project demand and notify interested actors. | At-least-once delivery; projection writes must be idempotent. |
| AllocationChanged | Booking / Allocation Service | DataHub, Notification, Audit | Keep read models, notifications, and evidence aligned with allocation lifecycle. | Preserve event order per aggregate where required; retries must not duplicate side effects. |
