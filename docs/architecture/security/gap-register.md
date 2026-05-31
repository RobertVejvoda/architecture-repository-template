# Gap Register

<!--
Purpose:
Track known architecture, security, privacy, or operational gaps.

Use this page for:
- gap description
- risk/impact
- mitigation
- owner
- target resolution

Avoid:
- untriaged vulnerability details that should be handled privately
- vague improvement ideas without impact
-->

| Gap | Impact | Mitigation | Owner | Status |
| --- | --- | --- | --- | --- |
| Public ingress not validated for target profile. | Increased exposure risk before pilot or production. | Complete WAF, TLS, origin protection, and smoke validation. | Security Lead / Operations | Open |
| Restore evidence missing for authoritative stores. | Incident recovery cannot be proven. | Run restore drill and link evidence from readiness. | Operations | Open |
| Privileged action audit coverage incomplete. | Support or compliance review may lack proof of who changed what and why. | Add audit events/tests for privileged commands. | Domain Owner | Planned |
