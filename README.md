# Release branch proof of concept

**Repo:** https://github.com/isaac-gainline/release-branch-poc

## Active rollout: `release/2026-09-25` (target `v1.3.0`)

Release branch naming: **`release/YYYY-MM-DD`** (deploy date).

| Step | PR | Notes |
|------|-----|--------|
| Ticket → release | See open PRs | Branches from `main`; expect conflicts on shared copy/config |
| Release → main | — | After all tickets merged |

See [WORKFLOW.md](https://github.com/isaac-gainline/release-branch-poc/blob/release/2026-09-25/WORKFLOW.md) on the release branch.

## Previous rollout: `release/2026-09-18` (`v1.2.0`)

Completed via PR #16 into `main`.

## Tags

| Tag | Description |
|-----|-------------|
| `v1.2.0` | 18 Sep rollout |
| `v1.3.0` | Target for 25 Sep rollout |

## Legacy

Older examples used `release/next`. New rollouts use dated branches only.
