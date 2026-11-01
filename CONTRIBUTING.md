# Contributing

## Setup

1. Install Node 24 and pnpm 10. `corepack enable` reads the pinned version from `package.json`.
2. Copy `.env.example` to `.env`. Ask a maintainer for values. Never commit `.env`.
3. Run `pnpm install --frozen-lockfile`.
4. Run `pnpm build` and `pnpm test`.

## Branch and commit

- Branch from the default branch: `feat/short-name`, `fix/short-name`, `chore/short-name`.
- Commit with Conventional Commits: `feat(api): add key rotation endpoint`.
- Keep one logical change per pull request.
- Rebase on the default branch before you request review. Do not merge the default branch into your branch.

## Pull request checklist

- [ ] CI is green: lint, typecheck, tests, build.
- [ ] Tests cover the change, or the pull request explains why they cannot.
- [ ] No secrets, tokens or customer data in the diff.
- [ ] Documentation updated when behaviour changes.
- [ ] One approval from a code owner.

## Review

- Review for correctness, security and operability.
- Block on: leaked secrets, missing authorization, unbounded queries, silent error handling.
- Approve when the change is safe to deploy, not when it is perfect.

## Release

Maintainers tag releases. The tag drives the changelog and the image build. Do not deploy from a laptop.

## Questions

Open a discussion or ask in the platform channel.
