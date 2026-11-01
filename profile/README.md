# Hawiyat

We build the Hawiyat AI platform: an AI gateway, an application platform, and the services that run on them.

## What we run

| Area | Topic filter |
|---|---|
| Application platform | [topic:platform](https://github.com/orgs/Hawiyat-Org/repositories?q=topic%3Aplatform) |
| AI gateway | [topic:ai-gateway](https://github.com/orgs/Hawiyat-Org/repositories?q=topic%3Aai-gateway) |
| Customer applications | [topic:sales](https://github.com/orgs/Hawiyat-Org/repositories?q=topic%3Asales) |
| Observability | [topic:observability](https://github.com/orgs/Hawiyat-Org/repositories?q=topic%3Aobservability) |
| Infrastructure | [topic:infrastructure](https://github.com/orgs/Hawiyat-Org/repositories?q=topic%3Ainfrastructure) |
| Tools and skills | [topic:hawiyat](https://github.com/orgs/Hawiyat-Org/repositories?q=topic%3Ahawiyat) |

Repository names change. The topics are stable. Pinned repositories on the org page are the current core set.

## How we work

- Trunk-based. Short branches. Squash merge. The default branch is always deployable.
- Every change goes through a pull request with one approval and a green CI run.
- Every commit follows Conventional Commits. Releases are tagged and generated.
- Secrets never enter git. Use the environment or the secrets manager.
- A service ships with a Dockerfile, a health endpoint, tests and a runbook link.

## Start here

- [Security policy](./SECURITY.md)
- [Contributing](./CONTRIBUTING.md)
- [Code of conduct](./CODE_OF_CONDUCT.md)

Reusable pipelines live in `.github/workflows/` of this repository. Call one from a repo:

```yaml
jobs:
  ci:
    uses: Hawiyat-Org/.github/.github/workflows/node-ci.yml@main
```

## Contact

security@hawiyat.org for vulnerabilities. contact@hawiyat.org for everything else.
