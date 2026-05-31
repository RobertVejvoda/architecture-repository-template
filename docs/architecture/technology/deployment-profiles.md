# Deployment Profiles

<!--
Purpose:
Describe supported deployment shapes and how they differ.

Use this page for:
- local, test, staging, production, or customer-owned profiles
- ingress and network boundaries
- platform dependencies
- environment-specific responsibilities

Avoid:
- credentials
- step-by-step runbooks unless needed for architecture review
-->

| Profile | Purpose | Key Components | Responsibilities |
| --- | --- | --- | --- |
| Local Development | Developer workflow and automated validation. | Local services, local dependencies, test identity, lightweight observability. | Development team owns setup and reset scripts. |
| Hosted Pilot | Controlled customer or stakeholder evaluation. | Public ingress, managed identity, persistent stores, monitoring, backup evidence. | Product/operator owns readiness and support boundary. |
| Customer-Owned Production | Deployment into a customer-controlled environment. | Customer-approved ingress, identity, data stores, secrets, observability. | Shared responsibilities must be documented before handoff. |
