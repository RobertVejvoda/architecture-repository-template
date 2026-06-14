# Privacy Architecture

<!--
Purpose:
Describe privacy-significant data flows, minimisation, retention, subject rights, and evidence needs.
-->

| Data / Flow | Purpose | Minimisation Rule | Retention / Disposal | Subject Rights / Review |
| --- | --- | --- | --- | --- |
| User profile and contact data | Identity, access, support, and communication. | Store only fields required for approved user journeys and operations. | Retain according to account lifecycle and legal obligations. | Subject access/export uses approved privacy workflow. |
| Core domain history | Service operation, dispute handling, audit, and reporting. | User views show only permitted records; aggregate views avoid unnecessary personal detail. | Retain for operational and legal evidence windows. | Subject access/export uses approved privacy workflow. |
| Audit events | Security, compliance, support, and incident evidence. | Audit records include required context but avoid secrets and unnecessary payload data. | Retain according to audit and security policy. | Access limited to approved roles; export reviewed. |
| Operational telemetry | Reliability, troubleshooting, and capacity management. | Logs and traces avoid secrets and unnecessary personal data. | Retain according to observability and privacy policy. | Review telemetry exports before external sharing. |

## Privacy Rules

- Identify personal or sensitive data in each architecture-significant flow.
- Keep role-safe outputs separate from internal diagnostics.
- Document retention, erasure, export, and restore-time re-erasure expectations.
- Record privacy gaps or waivers explicitly.
