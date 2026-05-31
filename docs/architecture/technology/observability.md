# Observability

<!--
Purpose:
Describe logs, metrics, traces, alerts, dashboards, and operational evidence.

Use this page for:
- telemetry model
- correlation IDs
- service health
- alerting principles
- audit versus technical telemetry boundaries

Avoid:
- raw log dumps
- environment-specific credentials
-->

| Signal | Purpose | Retention | Owner |
| --- | --- | --- | --- |
| Logs | Diagnose service behavior, exceptions, and operator-visible failures. | Project-defined period based on support and privacy needs. | Operations |
| Metrics | Track health, performance, saturation, and business-critical processing lag. | Short-to-medium operational window plus dashboard history. | Operations |
| Traces | Correlate user/API/event flows across services. | Short diagnostic window; avoid retaining sensitive payloads. | Operations / Architecture |
