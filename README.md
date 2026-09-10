# Release branch proof of concept

**Repo:** https://github.com/isaac-gainline/release-branch-poc

## Active rollout: `release/2026-09-18` (target `v1.2.0`)

Release branch naming: **`release/YYYY-MM-DD`** (deploy date).

| Step | PR | Notes |
|------|-----|--------|
| Ticket → release | [#11](https://github.com/isaac-gainline/release-branch-poc/pull/11) SES-3001 | Branch from `main` |
| Ticket → release | [#12](https://github.com/isaac-gainline/release-branch-poc/pull/12) SES-3005 | Branch from `main` |
| Ticket → release | [#13](https://github.com/isaac-gainline/release-branch-poc/pull/13) SES-3010 | Branch from `main` |
| Release → main | — | After all tickets merged |

See [WORKFLOW.md](https://github.com/isaac-gainline/release-branch-poc/blob/release/2026-09-18/WORKFLOW.md) on the release branch.

## Tags

| Tag | Description |
|-----|-------------|
| `v1.1.1` | Current production |
| `v1.2.0` | Target for 18 Sep rollout |

## Legacy

Older examples used `release/next`. New rollouts use dated branches only.
