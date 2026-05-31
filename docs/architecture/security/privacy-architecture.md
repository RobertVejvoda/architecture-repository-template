# Privacy Architecture

<!--
Purpose:
Describe privacy-by-design decisions, personal data handling, retention, and rights workflows.

Use this page for:
- personal data inventory
- lawful basis or processing purpose
- minimization and pseudonymization
- retention and deletion
- access and erasure workflows

Avoid:
- dumping personal data examples
- legal claims without review
-->

| Data Subject / Data Area | Purpose | Minimization | Retention | Rights Handling |
| --- | --- | --- | --- | --- |
| Employee profile facts | Eligibility, personalization, and operational contact. | Store only fields needed by approved workflows. | Retain while employment/account relationship is active plus policy-defined period. | Access/correction through profile or support workflow. |
| Request and allocation history | Service operation, dispute handling, audit, and reporting. | Employee views show only own records; aggregate views avoid unnecessary personal detail. | Retain for operational and legal evidence windows. | Subject access/export uses approved privacy workflow. |
| Technical telemetry | Security, reliability, and incident diagnosis. | Avoid raw personal payloads and secrets in logs/traces. | Short operational retention unless incident/legal hold applies. | Deletion or masking handled through log-retention policy. |
