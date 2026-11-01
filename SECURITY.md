# Security policy

## Supported versions

The latest release of each repository is supported. Older releases get fixes for critical issues for 90 days.

## Report a vulnerability

Email security@hawiyat.org. Do not open a public issue.

Include: affected service, version or commit, reproduction steps, and impact.

We acknowledge within 2 business days. We fix critical issues within 7 days. We credit reporters in the release notes unless you ask us not to.

## Scope

Any Hawiyat service, repository, or host. This covers the platform, the AI gateway, customer applications, the edge
services, and the infrastructure that runs them. Repository names change; the scope does not.

## Rules of engagement

- Do not access data that is not yours.
- Do not run denial-of-service tests.
- Do not scan production without written approval.
- Give us 90 days to fix an issue before you publish.

## What we do

- Dependabot alerts and security updates on every repository.
- Secret scanning and push protection on every public repository.
- Gitleaks in CI as a second check.
- Signed images and an SBOM for every production build.
