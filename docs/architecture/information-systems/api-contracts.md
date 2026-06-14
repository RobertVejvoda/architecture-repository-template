# API Contracts

<!--
Purpose:
Index architecture-significant API contracts and their source of truth.
-->

| API / Contract | Owner | Source Of Truth | Architecture Notes |
| --- | --- | --- | --- |
| User Experience API | Core Domain Service | OpenAPI, generated client, or source contract link | User-safe shape must not expose internal decision details or unrelated data. |
| Operations API | Core Domain Service / Operations Owner | OpenAPI, generated client, or source contract link | Privileged actions require authorization, reason capture, and audit evidence where applicable. |
| Reporting API | Read Model / Reporting Service | OpenAPI, generated client, or source contract link | Outputs must be role-safe, scoped, and traceable to source data. |
| Audit API | Audit Service | OpenAPI, generated client, or source contract link | Exports and privileged reads require explicit control review. |

## Contract Rules

- Link to source-of-truth contracts where possible.
- Record any narrative-only contract as a gap if consumers depend on it.
- Keep externally visible shapes separate from internal diagnostics.
