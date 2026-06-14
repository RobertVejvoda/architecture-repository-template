# Implementation And Migration

<!--
Purpose:
Describe how the target architecture will be reached through transition states, work packages, and readiness checks.

Use this page for:
- implementation and migration overview
- transition architecture links
- roadmap and work package links
- readiness model

Avoid:
- replacing project management tools
- detailed sprint/task status unless architecture-significant
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.1</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Transition / Migration</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Phases E/F/G</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

## Contents

- [Migration Roadmap](/architecture/implementation-migration/roadmap.md)
- [Work Packages](/architecture/implementation-migration/work-packages.md)
- [Delivery Sourcing Options](/architecture/implementation-migration/delivery-sourcing-options.md)
- [Architecture Increment Checklist](/architecture/implementation-migration/vertical-slice-checklist.md)
- [Readiness](/architecture/implementation-migration/readiness.md)
- [Transition Architectures](/architecture/architecture-states/transition-architectures.md)

## Requirement Coverage

Use this section to show how Implementation and Migration interprets central requirements from [Requirements Management](/architecture/requirements.md). Requirements become work packages, readiness evidence, release checks, accepted risks, or deferred gaps here.

| Requirement | Implementation / Migration Interpretation | Impacted Artifacts | Evidence / Gap |
| --- | --- | --- | --- |
| AR-002 | Restart-safe operational state must be validated through work packages and readiness evidence before pilot or production handoff. | Roadmap, Work Packages, Readiness. | Link restore evidence, smoke results, and residual risk decisions. |
| AR-004 | Target-state changes must remain traceable to gaps, work packages, readiness, and architecture versions. | Roadmap, Work Packages, Architecture Version Register. | Link change sets and delivery evidence where relevant. |
