# Waivers

<!--
Purpose:
Track approved exceptions to architecture principles, standards, or controls.

Use this page for:
- exception description
- rationale
- risk owner
- expiry or review date
- mitigation

Avoid:
- permanent exceptions without review
- undocumented risk acceptance
-->

| Waiver | Standard / Principle | Rationale | Risk Owner | Review Date | Status |
| --- | --- | --- | --- | --- | --- |
| Local-only secret substitute | Secrets outside source code | Local development may use a non-production substitute when clearly marked and excluded from customer traffic. | Operations | YYYY-MM-DD | Proposed |
| Manual readiness step | Evidence Before Approval | A readiness check may remain manual for pilot if owner, evidence, and replacement plan are documented. | Architecture Board | YYYY-MM-DD | Proposed |
| Deferred dashboard automation | Operational readiness standard | Manual operational report accepted temporarily while event-fed read model is built. | Operations Owner | YYYY-MM-DD | Proposed |
