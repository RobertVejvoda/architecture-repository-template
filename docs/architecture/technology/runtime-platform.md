# Runtime Platform

<!--
Purpose:
Describe the runtime platform and technology standards used by applications.

Use this page for:
- language/runtime choices
- platform services
- middleware
- persistence technology classes
- resilience standards

Avoid:
- vendor-specific instructions unless selected as target architecture
- secrets or environment values
-->

| Technology Area | Standard / Direction | Rationale | Notes |
| --- | --- | --- | --- |
| Service Runtime | Containerized services with explicit health checks and configuration boundaries. | Supports repeatable local, demo, and production profiles. | Runtime-specific details belong in deployment profiles. |
| State And Events | Service-owned persistence plus asynchronous events for read models and evidence. | Keeps command ownership clear and enables operational views. | Use outbox or equivalent reliability pattern where state and events must be atomic. |
| Secrets And Identity | Externalized secrets and trusted identity provider integration. | Avoids committed credentials and centralizes authentication. | Local development may use safe substitutes clearly marked as non-production. |
