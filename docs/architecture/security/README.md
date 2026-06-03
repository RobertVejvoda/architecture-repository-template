# Security Architecture

<!--
Purpose:
Describe security and privacy architecture as cross-cutting concerns.

Use this page for:
- security architecture overview
- privacy model
- control catalog
- known gaps
- security review entry points

Avoid:
- secrets
- vulnerability details that should not be public
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Target</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Cross-cutting Security / Privacy</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Security Lead</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

## Contents

- [Security Architecture](/architecture/security/security-architecture)
- [Privacy Architecture](/architecture/security/privacy-architecture)
- [Controls](/architecture/security/controls)
- [Gap Register](/architecture/security/gap-register)

## Requirement Coverage

Use this section to show how Security and Privacy Architecture interprets central requirements from [Requirements Management](/architecture/requirements). Keep the central requirement stable; record control, privacy, threat, audit, and accepted-risk consequences here.

| Requirement | Security / Privacy Interpretation | Impacted Artifacts | Evidence / Gap |
| --- | --- | --- | --- |
| AR-001 | Role and organizational scope must be enforced consistently across identity, authorization, API, audit, and user-facing views. | Security Architecture, Controls, Gap Register. | Validate authorization tests and privileged-access review evidence. |
| AR-FS-001 | FairSpot sample: tenant and employee data must be protected across APIs, persistence, events, audit, and read models. | Security Architecture, Privacy Architecture, Controls. | Prove tenant isolation and privacy minimisation in projections and exports. |
