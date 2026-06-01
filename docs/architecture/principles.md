# Architecture Principles

<!--
Purpose:
Record stable architecture principles that guide decisions across the repository.

Use this page for:
- principle name
- statement
- rationale
- implications

Avoid:
- vague slogans
- implementation preferences that are not durable
-->

| Principle | Statement | Rationale | Implications |
| --- | --- | --- | --- |
| Own Your Data | Each bounded context owns its authoritative write model. | Prevents hidden coupling and unclear accountability. | Cross-service reads use APIs, events, or approved read models rather than private store access. |
| Secure By Default | Sensitive data and privileged actions require explicit authorization, auditability, and least privilege. | Security posture should not depend on UI hiding or convention. | APIs derive actor/context from trusted identity; exceptions require review or waiver. |
| Evidence Before Approval | Architecture status moves forward only when supporting evidence is linked. | Reduces paper architecture and unverifiable assumptions. | Gaps, work packages, reviews, and readiness checks must link to implementation or validation evidence. |
