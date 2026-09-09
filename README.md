# Release branch proof of concept

A minimal repo demonstrating the `release/next` rollout workflow used by GAIN LINE.

**Repo:** https://github.com/isaac-gainline/release-branch-poc

## Quick start

Read [WORKFLOW.md](WORKFLOW.md) on `release/next` for the current walkthrough.

## Tags

| Tag | Description |
|-----|-------------|
| `v1.0.0` | Initial baseline |
| `v1.1.0` | Rollout 1 complete |
| `v1.2.0` | **Target** for rollout 2 (in progress) |

## Rollout 2 state (mid-week)

- [x] `release/next` reset from `main` at `v1.1.0`
- [x] [PR #7](https://github.com/isaac-gainline/release-branch-poc/pull/7) SES-2849 merged into `release/next`
- [ ] [PR #8](https://github.com/isaac-gainline/release-branch-poc/pull/8) SES-2861 open — **merge next**
- [ ] SES-2901 PR — create and merge after #8
- [ ] PR `release/next` → `main`
- [ ] Tag `v1.2.0`

## Rollout 1 (complete)

PRs #1, #4, #5 → `release/next`, then #6 → `main`. Released as `v1.1.0`.
