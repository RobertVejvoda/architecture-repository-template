# Security Controls

<!--
Purpose:
Record control expectations, evidence, owner, and status.
-->

| Control ID | Control | Evidence | Owner | Status |
| --- | --- | --- | --- | --- |
| SEC-001 | APIs derive actor, role, and scope from trusted authentication context. | API contract, authorization tests, architecture review evidence. | Security Lead | Planned |
| SEC-002 | Privileged actions are audited with actor, reason, timestamp, and affected entity where applicable. | Audit contract, test evidence, review sample. | Security Lead | Planned |
| SEC-003 | Public endpoints use approved ingress, TLS, logging, and abuse-prevention profile. | Deployment profile, smoke tests, ingress/WAF evidence. | Operations / Security | Planned |
| SEC-004 | Backup, restore, export, and support operations preserve data boundaries and avoid exposing secrets. | Runbooks, restore test, access review. | Operations / Security | Planned |
