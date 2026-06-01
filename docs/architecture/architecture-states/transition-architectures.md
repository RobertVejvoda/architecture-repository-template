# Transition Architectures

<!--
Purpose:
Describe intermediate architecture states between baseline and target.

Use this page for:
- migration increments
- release architecture states
- dependency sequencing
- transition risks

Avoid:
- detailed sprint plans
- transitions that do not change architecture capability
-->

| Transition | From Version | To Version | Capabilities Added | Risks | Exit Criteria |
| --- | --- | --- | --- | --- | --- |
| T1 | Current State v0.1 | Foundation Target v0.1 | Architecture repository, principles, requirements, governance, and baseline evidence. | Stakeholder assumptions may remain incomplete. | Artifact register and initial decision log reviewed. |
| T2 | Foundation Target v0.1 | Pilot Target v0.1 | Durable state, protected ingress, readiness checks, and first operational views. | Accepted limitations must be explicit and time-bound. | Critical gaps closed or waived with linked evidence. |
| T3 | Pilot Target v0.1 | Production Target v0.1 | Restore drills, observability, operational runbooks, and conformance evidence. | Operational process may become too heavy if not pruned. | Architecture Board accepts readiness and residual risk. |
