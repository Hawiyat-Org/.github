# Hawiyat org defaults

This public repository holds the files GitHub applies to every repository in the `Hawiyat-Org` organization.

## What is inherited automatically

GitHub uses these files in any repository that does not have its own copy:

| File | Scope |
|---|---|
| `SECURITY.md` | Security tab and community profile |
| `CONTRIBUTING.md` | Community profile and new issue and PR links |
| `CODE_OF_CONDUCT.md` | Community profile |
| `PULL_REQUEST_TEMPLATE.md` | New pull requests |
| `ISSUE_TEMPLATE/*.yml` | New issues |
| `profile/README.md` | The organization landing page |

## What is not inherited

- `.github/dependabot.yml` here configures Dependabot for this repository only. Each repository needs its own copy.
  Copy it with `cp .github/dependabot.yml <repo>/.github/dependabot.yml`.
- `.github/workflows/*.yml` are reusable pipelines. They do not run here. Another repository calls them with `uses:`.

## How to call a reusable pipeline

```yaml
jobs:
  ci:
    uses: Hawiyat-Org/.github/.github/workflows/node-ci.yml@main
    with:
      coverage-threshold: 60

  image:
    uses: Hawiyat-Org/.github/.github/workflows/docker-build.yml@main
    with:
      image-name: hawiyat-org/example
      push: true
    permissions:
      contents: read
      packages: write
      id-token: write
      attestations: write
      security-events: write

  secrets:
    uses: Hawiyat-Org/.github/.github/workflows/secret-scan.yml@main
```

## Rules for this repository

- Action references are pinned to commit SHAs. Dependabot updates the pins weekly.
- `main` is the only branch. Change through a pull request.
- This repository is public on purpose. Inheritance only works from a public `.github` repository.

## Related

- Security contact: security@hawiyat.org
