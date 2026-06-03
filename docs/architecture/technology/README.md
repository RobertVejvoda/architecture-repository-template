# Technology Architecture

<!--
Purpose:
Describe runtime technology choices, deployment profiles, and operational platform direction.

Use this page for:
- technology architecture overview
- runtime standards
- approved technology standards
- deployment profiles
- observability and resilience

Avoid:
- application business logic
- environment-specific secrets
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Target</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Phase D</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

## Contents

- [Runtime Platform](/architecture/technology/runtime-platform)
- [Deployment Profiles](/architecture/technology/deployment-profiles)
- [Technology Standards](/architecture/technology/standards)
- [Observability](/architecture/technology/observability)

## Requirement Coverage

Use this section to show how Technology Architecture interprets central requirements from [Requirements Management](/architecture/requirements). Keep non-functional requirement ownership central; record runtime, platform, deployment, observability, backup, and operational consequences here.

| Requirement | Technology Interpretation | Impacted Artifacts | Evidence / Gap |
| --- | --- | --- | --- |
| AR-002 | Operational state needed for pilot or production must survive restart and have backup/restore evidence. | Runtime Platform, Deployment Profiles, Observability. | Validate state-store profile, backup/restore procedure, and restore evidence. |
| AR-003 | Public-facing surfaces must be protected by an approved ingress, identity, logging, and abuse-prevention profile. | Deployment Profiles, Technology Standards, Observability. | Prove the selected ingress/WAF/auth profile before production use. |
