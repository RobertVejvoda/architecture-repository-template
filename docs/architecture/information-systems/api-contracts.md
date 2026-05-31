# API Contracts

<!--
Purpose:
Index API contracts and explain contract ownership and compatibility rules.

Use this page for:
- API catalog
- contract location
- versioning rules
- compatibility expectations

Avoid:
- hand-copying generated OpenAPI content
- implementation-specific controller details
-->

| API | Owner | Contract Location | Versioning / Compatibility |
| --- | --- | --- | --- |
| Tenant Readiness API | Customer / Tenant Service | OpenAPI or source contract link | Additive changes preferred; readiness states must remain backward compatible. |
| Request Lifecycle API | Booking / Allocation Service | OpenAPI or source contract link | Employee-safe shape must not expose hidden decision internals. |
| Projection Health API | DataHub / Read Model Service | OpenAPI or source contract link | Must expose safe lag/failure metadata without raw private payloads. |
