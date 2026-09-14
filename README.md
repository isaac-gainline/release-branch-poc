# Release branch proof of concept

**Repo:** https://github.com/isaac-gainline/release-branch-poc

## Active rollout: `release/2026-09-25` (target `v1.3.0`)

Release branch naming: **`release/YYYY-MM-DD`** (deploy date).

| Step | PR | Notes |
|------|-----|--------|
| Ticket → release | [#17](https://github.com/isaac-gainline/release-branch-poc/pull/17) SES-3101 | **Merged** (merge commit) |
| Ticket → release | [#18](https://github.com/isaac-gainline/release-branch-poc/pull/18) SES-3105 | Conflicts until synced |
| Ticket → release | [#19](https://github.com/isaac-gainline/release-branch-poc/pull/19) SES-3110 | Conflicts until synced |
| Ticket → release | [#20](https://github.com/isaac-gainline/release-branch-poc/pull/20) SES-3112 | Conflicts until synced |
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
