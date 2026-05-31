# Business Policies

<!--
Purpose:
Record business rules and policy decisions that architecture and implementation must respect.

Use this page for:
- policy statements
- eligibility rules
- prioritization rules
- approval and exception rules
- policy ownership

Avoid:
- source code constants
- UI copy
-->

| Policy | Rule | Owner | Notes |
| --- | --- | --- | --- |
| Eligibility Policy | Only eligible users may request or receive constrained resources. | Business Owner | Eligibility source must be authoritative and auditable. |
| Cancellation Policy | Privileged cancellation requires reason, audit evidence, and user notification where applicable. | Operations Owner | Retry must not duplicate side effects. |
| Readiness Policy | Customer or tenant traffic may start only after mandatory readiness checks pass or are formally waived. | Architecture Board | Waivers need owner and review date. |
