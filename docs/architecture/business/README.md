# Business Architecture

<!--
Purpose:
Describe the business shape independent of software implementation.

Use this page for:
- business architecture overview
- links to capabilities, value streams, actors, processes, and policies
- major business assumptions and constraints

Avoid:
- application component design
- database or API details
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

Business architecture explains what the organization needs to do and why it matters.

## Contents

- [Capabilities](architecture/business/capabilities.md)
- [Value Streams](architecture/business/value-streams.md)
- [Actors and Roles](architecture/business/actors-roles.md)
- [Business Processes](architecture/business/business-processes.md)
- [Policies](architecture/business/policies.md)

## Requirement Interpretation Sample

Use this section to show how Business Architecture interprets central requirements from [Requirements Management](architecture/requirements.md). Do not duplicate the central requirement as a new competing requirement.

| Requirement | Business Interpretation | Evidence | Gap |
| --- | --- | --- | --- |
| AR-FS-001 | FairSpot sample: business roles and processes must not expose or act on another tenant's requests, people, policy, or reports. | Actors and Roles, Business Processes, Policies. | Validate privileged support/HR actions against tenant boundary. |
