# Release branch proof of concept

A minimal repo demonstrating the `release/next` rollout workflow used by GAIN LINE.

**Repo:** https://github.com/isaac-gainline/release-branch-poc

## Quick start

Read [WORKFLOW.md](WORKFLOW.md) for the hands-on walkthrough.

## Branches

| Branch | Purpose |
|--------|---------|
| `main` | Production-ready code. Tagged for deploy. |
| `release/next` | Integration branch for the upcoming rollout |
| `SES-*` branches | Individual ticket work |

## Tags

| Tag | Description |
|-----|-------------|
| `v1.0.0` | Baseline on `main` before the example rollout week |
| `v1.1.0` | Create after merging `release/next` into `main` (see WORKFLOW.md) |

## Current POC state (mid-week)

- [x] `release/next` created from `main`
- [x] [PR #1](https://github.com/isaac-gainline/release-branch-poc/pull/1) SES-1380 merged into `release/next`
- [x] [PR #4](https://github.com/isaac-gainline/release-branch-poc/pull/4) SES-1392 merged into `release/next`
- [ ] [PR #5](https://github.com/isaac-gainline/release-branch-poc/pull/5) SES-1400 open — **merge this to continue**
- [ ] PR `release/next` → `main` — do after all tickets merged
- [ ] Tag `v1.1.0` on `main`

## Release notes on GitHub

After tagging `v1.1.0`, create a release and click **Generate release notes**. Compare range: `v1.0.0...v1.1.0`.

Each ticket PR merged into `release/next` should appear as its own line when `release/next` is merged into `main`.
