# Release branch proof of concept

**Repo:** https://github.com/isaac-gainline/release-branch-poc

## Rollout 2 (in progress)

See [WORKFLOW.md](https://github.com/isaac-gainline/release-branch-poc/blob/release/next/WORKFLOW.md) on `release/next`.

| Step | PR | Status |
|------|-----|--------|
| SES-2849 → `release/next` | [#7](https://github.com/isaac-gainline/release-branch-poc/pull/7) | Merged |
| SES-2861 → `release/next` | [#8](https://github.com/isaac-gainline/release-branch-poc/pull/8) | Merged |
| SES-2901 → `release/next` | [#9](https://github.com/isaac-gainline/release-branch-poc/pull/9) | Open |
| `release/next` → `main` | [#10](https://github.com/isaac-gainline/release-branch-poc/pull/10) | After #9 |
| Tag `v1.2.0` | — | After rollout merge |

## Tags

| Tag | Description |
|-----|-------------|
| `v1.1.0` | Rollout 1 complete |
| `v1.2.0` | Target for rollout 2 |

## Rollout 1 (complete)

PRs #1, #4, #5 → `release/next`, then #6 → `main`. Released as `v1.1.0`.
