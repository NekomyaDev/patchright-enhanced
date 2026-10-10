# Contributing to patchright-enhanced

Bug reports, documentation, UX proposals, and focused pull requests are welcome.
Read the [code of conduct](CODE_OF_CONDUCT.md) and [roadmap](ROADMAP.md) first.

## Local setup

Use Node.js 20 or newer and pnpm. From your fork's checkout:

```bash
pnpm install
pnpm exec patchright install chrome
cp .env.example .env
```

Configure `.env` and a local, gitignored `proxies.txt` as described in the
[README](readme.md). Use test accounts and systems you own or have permission to test.

```bash
pnpm exec tsc --noEmit
pnpm build
pnpm dev
```

`pnpm dev` launches real browser sessions in a repeating loop. Stop the process
with Ctrl+C when finished. There is currently no automated test suite or lint command.

## Issues and proposals

- Search existing issues before opening a new one; use the bug or feature template.
- For bugs, include a minimal reproduction, expected and actual behavior, OS,
  Node.js, pnpm, Chrome, and Patchright versions, and sanitized logs.
- Discuss substantial architecture changes, new dependencies, and UI/UX flows in
  an issue before implementation. Mockups and interaction descriptions are welcome.
- Report vulnerabilities through the [security policy](SECURITY.md), not a public issue.

## Pull requests

1. Create a focused branch from the current default branch.
2. Keep changes small and follow the existing TypeScript architecture and naming.
3. Update relevant documentation and `.env.example` when behavior or configuration changes.
4. Run `pnpm exec tsc --noEmit` and `pnpm build`. For browser changes, describe a
   manual smoke test, including startup, the changed behavior, and session cleanup.
5. Add regression tests for changes to business logic, parsing, matching, money,
   odds, authentication, or security. If test tooling is needed, keep it scoped
   and document how to run it. Documentation-only changes need link and diff checks.
6. Explain the problem, resulting behavior, verification, and any limitations in the PR.

Never commit credentials, proxy passwords, cookies, browser profiles, tokens,
personal data, or unsanitized screenshots and traces. Keep unrelated reformatting
and dependency updates out of a PR. Maintainers review scope, correctness,
security, and reproducibility before merging; response times are not guaranteed.
