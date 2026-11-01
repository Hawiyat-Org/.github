# Hawiyat

The AI execution layer, built in Algeria. One API key for GPT, Claude, Gemini and open models, billed in DZD.

[Website](https://hawiyat.org) · [Blog](https://hawiyat.org/blog) · [Pricing](https://hawiyat.org/pricing) · [API](https://hawiyat.org/api)

## Products

| Product | What it does | Links |
|---|---|---|
| **Hawiyat AI Composer** | Stateful execution layer. It picks the model per task, connects your systems, and checks the result before it ships. | [Plans](https://hawiyat.org/composer) · [Pricing](https://hawiyat.org/pricing) |
| **Hawiyat API** | One OpenAI-compatible key for GPT, Claude, Gemini and open models. DZD billing, CCP and Baridi Mob, no foreign card. | [API](https://hawiyat.org/api) · [AI API in Algeria](https://hawiyat.org/ai-api-algeria) |
| **Managed automation** | n8n hosting, WhatsApp Business API on Evolution API, and application hosting. Activated in 24 hours. | [Services](https://hawiyat.org/services) |
| **Enterprise** | Dedicated capacity, custom infrastructure, named account manager, AR/FR/EN support. | [Pricing](https://hawiyat.org/pricing) |

## From the blog

- [GLM-5.3-Flash Uncensored: How Abliteration Removes Refusal From an Open Model](https://hawiyat.org/blog/glm-5-3-flash-uncensored-abliteration) · 2026-10-15
- [AI API in Algeria (2026): Hawiyat vs DZRouter vs OpenDunes](https://hawiyat.org/blog/best-ai-provider-algeria-comparison) · 2026-10-15
- [We Audited the Same Codebase with Hawiyat Composer and Claude Opus 4.8](https://hawiyat.org/blog/hawiyat-composer-vs-claude-opus-benchmark) · 2026-08-17
- [What Is Hawiyat Composer?](https://hawiyat.org/blog/what-is-hawiyat-composer) · 2026-08-17
- [n8n Hosting in Algeria: DZD Pricing, Setup, and What You Get](https://hawiyat.org/blog/n8n-hosting-algeria-guide) · 2026-08-17
- [WhatsApp Business API in Algeria: A Practical Guide with Evolution API](https://hawiyat.org/blog/whatsapp-business-api-algeria) · 2026-08-17

[All posts](https://hawiyat.org/blog) · [RSS](https://hawiyat.org/feed.xml)

## How we work

- Trunk-based. Short branches. Squash merge. The default branch is always deployable.
- Every change goes through a pull request with one approval and a green CI run.
- Every commit follows Conventional Commits. Releases are tagged and generated.
- Secrets never enter git. Use the environment or the secrets manager.
- A service ships with a Dockerfile, a health endpoint, tests and a runbook link.

## Default configs

Copy these into a repository. GitHub does not inherit them from here.

**Dependabot.** Weekly updates for npm, pip, Docker and GitHub Actions, grouped by ecosystem. It also keeps SHA-pinned actions current.

```bash
mkdir -p .github
curl -fsSL https://raw.githubusercontent.com/Hawiyat-Org/.github/main/.github/dependabot.yml \
  -o .github/dependabot.yml
```

[View dependabot.yml](https://github.com/Hawiyat-Org/.github/blob/main/.github/dependabot.yml) · [Raw](https://raw.githubusercontent.com/Hawiyat-Org/.github/main/.github/dependabot.yml)

**Reusable pipelines.** Call them instead of copying YAML.

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

  secrets:
    uses: Hawiyat-Org/.github/.github/workflows/secret-scan.yml@main
```

[node-ci](https://github.com/Hawiyat-Org/.github/blob/main/.github/workflows/node-ci.yml) ·
[docker-build](https://github.com/Hawiyat-Org/.github/blob/main/.github/workflows/docker-build.yml) ·
[secret-scan](https://github.com/Hawiyat-Org/.github/blob/main/.github/workflows/secret-scan.yml)

**Policy.** Inherited by every repository without a local copy.

[Security](https://github.com/Hawiyat-Org/.github/blob/main/SECURITY.md) ·
[Contributing](https://github.com/Hawiyat-Org/.github/blob/main/CONTRIBUTING.md) ·
[Code of conduct](https://github.com/Hawiyat-Org/.github/blob/main/CODE_OF_CONDUCT.md)

## Contact

security@hawiyat.org for vulnerabilities. contact@hawiyat.org for everything else.
WhatsApp: [+213 559 555 951](https://wa.me/213559555951). Arabic, French, English.
