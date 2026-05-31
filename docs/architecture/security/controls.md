# Controls

<!--
Purpose:
Catalog security and privacy controls that support architecture requirements.

Use this page for:
- control ID
- control statement
- implementation or evidence link
- owner
- status

Avoid:
- sensitive control bypass details
- raw scanner output
-->

| Control ID | Control | Evidence | Owner | Status |
| --- | --- | --- | --- | --- |
| SEC-001 | APIs derive tenant, actor, and role from trusted authentication context. | API contract, authorization tests, architecture review evidence. | Security Lead | Planned |
| SEC-002 | Secrets are stored outside source code and injected through approved runtime mechanisms. | Deployment profile, secret-store configuration, repository scan evidence. | Operations | Planned |
| SEC-003 | Privileged actions produce audit evidence with actor, target, reason, and timestamp. | Audit contract, event evidence, implementation tests. | Security Lead / Domain Owner | Planned |
