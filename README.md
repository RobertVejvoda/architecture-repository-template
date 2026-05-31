# Architecture Repository Template

Reusable documentation skeleton for a lightweight architecture repository inspired by TOGAF 10 and the ADM cycle.

The template is intentionally documentation-first. It gives teams a place to record architecture vision, stakeholder concerns, business architecture, information systems architecture, technology architecture, security views, implementation planning, governance, and diagrams without forcing every TOGAF artifact into the repository.

## Use This Template

1. Copy the `docs/` directory into your project or use this repository as a starting point.
2. Replace placeholder guidance with project-specific content.
3. Keep architecture decisions in version control and review them through pull requests.
4. Keep implementation evidence separate from target architecture unless it is needed for architecture governance.

## Structure

| Area | Purpose |
| --- | --- |
| `docs/architecture/` | Architecture repository entry point and ADM map. |
| `docs/architecture/business/` | Business capabilities, actors, value streams, processes, and policies. |
| `docs/architecture/information-systems/` | Application, data, service, API, and integration architecture. |
| `docs/architecture/technology/` | Runtime platform, deployment profiles, observability, and technology standards. |
| `docs/architecture/security/` | Security, privacy, controls, and known gaps. |
| `docs/architecture/implementation-migration/` | Roadmap, transition architectures, work packages, and readiness. |
| `docs/architecture/governance/` | Review process, change control, waivers, and architecture board guidance. |
| `docs/architecture/views/` | Viewpoint catalog and diagram index. |

## Local Preview

The `docs/` folder is a Docsify site. You can preview it with any static file server or the Docsify CLI.

```bash
npx docsify-cli serve docs
```

## License

MIT. See [LICENSE](./LICENSE).
