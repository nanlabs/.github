# Danger Validation

This directory contains the shared Danger setup used by NaNLABS public
repositories.

## Local Checks

Run these commands before changing the Danger workflow or rules:

```bash
pnpm install --frozen-lockfile
pnpm exec tsc --noEmit
```

## PR Body Expectations

The Danger rules expect pull request descriptions to include these sections:

- `## Description`
- `## Type of Change`
- `## How Has This Been Tested?`
- `## Checklist`

Human-authored pull requests must also reference an issue in the title or
description, for example `Closes #123` or `Refs #123`. Bot and release PRs are
exempt so routine dependency/version automation can continue without noise.

Do not include GitHub tokens or secrets in local examples. Use repository
workflow credentials only inside GitHub Actions.
