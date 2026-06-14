# Business Architecture

<!--
Purpose:
Describe business capabilities, value streams, actors, processes, policies, and business requirement interpretation.

Use this page for:
- business architecture overview
- requirement interpretation for Phase B
- links to capability, value stream, actor, process, and policy artifacts

Avoid:
- detailed implementation design
- duplicating requirements that belong in Requirements Management
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Target</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Phase B</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Business Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

Business architecture explains the business shape of the solution. Keep detailed obligations in [Requirements](/architecture/requirements.md) and use this section to show business meaning, ownership, process, and policy context.

## Contents

- [Capabilities](/architecture/business/capabilities.md)
- [Value Streams](/architecture/business/value-streams.md)
- [Actors and Roles](/architecture/business/actors-roles.md)
- [Business Processes](/architecture/business/business-processes.md)
- [Policies](/architecture/business/policies.md)

## Requirement Coverage

| Requirement | Business Interpretation | Impacted Artifacts | Evidence / Gap |
| --- | --- | --- | --- |
| AR-001 | Business roles and processes must only expose data and actions that match responsibility and organizational scope. | Actors and Roles, Business Processes, Policies. | Validate privileged and support actions against business responsibility. |
| AR-004 | Business architecture must distinguish target business intent from implementation evidence and open gaps. | Capabilities, Value Streams, Business Processes. | Link gaps where business validation is incomplete. |
