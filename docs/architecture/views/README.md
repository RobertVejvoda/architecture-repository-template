# Views And Diagrams

<!--
Purpose:
Index stakeholder-specific architecture views and diagrams.

Use this page for:
- viewpoint catalog
- diagram index
- source model links
- diagram ownership and freshness

Avoid:
- scattering authoritative diagrams without an index
- unexplained diagrams with no stakeholder concern
-->

<table style="border:none;border-collapse:collapse;">
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Status</strong></td><td style="border:none;padding:3px 0;">Draft</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Version</strong></td><td style="border:none;padding:3px 0;">0.9</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Architecture State</strong></td><td style="border:none;padding:3px 0;">Cross-cutting</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>ADM Phase</strong></td><td style="border:none;padding:3px 0;">Cross-ADM</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Responsible</strong></td><td style="border:none;padding:3px 0;">Architecture Owner</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Accountable</strong></td><td style="border:none;padding:3px 0;">Architecture Board</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Last Reviewed</strong></td><td style="border:none;padding:3px 0;">2026-06-14</td></tr>
<tr style="border:none;"><td style="border:none;padding:3px 16px 3px 0;"><strong>Next Review</strong></td><td style="border:none;padding:3px 0;">-</td></tr>
</table>

## Contents

- [Viewpoint Catalog](/architecture/views/viewpoint-catalog)
- [Diagrams](/architecture/views/diagrams)

## View Versioning Rules

Views and diagrams are versioned separately from the architecture pages they support.

| Rule | Meaning |
| --- | --- |
| Architecture artifact owns the reviewed narrative | Business, information systems, technology, security, and other architecture pages own the accepted architecture text and metadata. |
| Diagram catalog owns diagram lifecycle | [Diagrams](/architecture/views/diagrams) tracks diagram version, status, source, export, owner, review date, and supported architecture version. |
| Architecture pages link related views | Architecture pages should reference relevant diagrams through a `Related Views` section, but should not duplicate the central diagram registry. |
| Mixed ArchiMate diagrams keep layer order | When a diagram spans layers, arrange business concepts above application concepts and application concepts above technology concepts. Motivation and implementation elements can sit above or beside the affected layer when that improves readability. |
| Text wins unless a diagram is authoritative | If a diagram is older than the architecture text, the architecture text is authoritative unless the diagram is explicitly marked authoritative for the named architecture version. |
| Source and export must stay traceable | A diagram row should identify both the editable source and the rendered export when both exist. |

Add viewpoints only when they answer a real stakeholder concern. A project does not need every possible diagram type.

## Diagram Status Values

| Status | Meaning |
| --- | --- |
| Placeholder | A diagram is needed but does not yet exist or has not been refreshed. |
| Source Evidence | Existing historical diagram or model that can inform target architecture but is not authoritative. |
| Draft | Diagram exists but has not been reviewed or approved. |
| In Review | Diagram is ready for stakeholder or architecture review. |
| Approved | Diagram is accepted for its stated scope. |
| Authoritative | Diagram is approved as a source of truth for a named architecture version. |
| Superseded | Diagram has been replaced by a newer diagram or version. |
