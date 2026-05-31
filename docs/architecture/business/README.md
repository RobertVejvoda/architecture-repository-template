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

Business architecture explains what the organization needs to do and why it matters.

## Contents

- [Capabilities](architecture/business/capabilities.md)
- [Value Streams](architecture/business/value-streams.md)
- [Actors and Roles](architecture/business/actors-roles.md)
- [Business Processes](architecture/business/business-processes.md)
- [Policies](architecture/business/policies.md)

## Requirement Interpretation Example

Use this section to show how Business Architecture interprets central requirements from [Requirements Management](architecture/requirements.md). Do not duplicate the central requirement as a new competing requirement.

| Requirement | Business Interpretation | Evidence | Gap |
| --- | --- | --- | --- |
| AR-FS-001 | FairSpot example: business roles and processes must not expose or act on another tenant's requests, people, policy, or reports. | Actors and Roles, Business Processes, Policies. | Validate privileged support/HR actions against tenant boundary. |
