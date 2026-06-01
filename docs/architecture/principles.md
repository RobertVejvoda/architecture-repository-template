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

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Cross-cutting</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Preliminary</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

| Principle | Statement | Rationale | Implications |
| --- | --- | --- | --- |
| Own Your Data | Each bounded context owns its authoritative write model. | Prevents hidden coupling and unclear accountability. | Cross-service reads use APIs, events, or approved read models rather than private store access. |
| Secure By Default | Sensitive data and privileged actions require explicit authorization, auditability, and least privilege. | Security posture should not depend on UI hiding or convention. | APIs derive actor/context from trusted identity; exceptions require review or waiver. |
| Evidence Before Approval | Architecture status moves forward only when supporting evidence is linked. | Reduces paper architecture and unverifiable assumptions. | Gaps, work packages, reviews, and readiness checks must link to implementation or validation evidence. |
