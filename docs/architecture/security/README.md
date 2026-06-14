# Security Architecture

<!--
Purpose:
Describe security, privacy, controls, and known trust gaps.
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Target</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Cross-cutting</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Security Lead</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

## Contents

- [Security Architecture](/architecture/security/security-architecture.md)
- [Privacy Architecture](/architecture/security/privacy-architecture.md)
- [Controls](/architecture/security/controls.md)
- [Gap Register](/architecture/security/gap-register.md)

## Requirement Coverage

| Requirement | Security / Privacy Interpretation | Impacted Artifacts | Evidence / Gap |
| --- | --- | --- | --- |
| AR-001 | Sensitive data and privileged actions must be protected across APIs, persistence, events, audit, and read models. | Security Architecture, Privacy Architecture, Controls. | Prove authorization, privacy minimisation, and audit behavior in implementation evidence. |
| AR-003 | Public-facing surfaces require approved ingress, identity, logging, monitoring, and abuse-prevention controls. | Security Architecture, Controls, Gap Register. | Link profile-specific validation or waiver. |
