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

Do not include GitHub tokens or secrets in local examples. Use repository
workflow credentials only inside GitHub Actions.
