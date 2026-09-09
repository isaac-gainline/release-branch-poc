# Release branch proof of concept

A minimal repo demonstrating the `release/next` rollout workflow used by GAIN LINE.

## Branches

| Branch | Purpose |
|--------|---------|
| `main` | Production-ready code. Tagged for deploy. |
| `release/next` | Integration branch for the upcoming rollout |
| `SES-*` branches | Individual ticket work |

## Tags

| Tag | Description |
|-----|-------------|
| `v1.0.0` | Baseline before the example rollout week |
| `v1.1.0` | Rollout after merging `release/next` into `main` |

## Example rollout (already applied in this repo)

1. `release/next` was created from `main` at `v1.0.0`
2. Ticket branches merged into `release/next` through the week:
   - `SES-1380`: Booking expiry fix
   - `SES-1392`: My account copy update
   - `SES-1400`: Upsells optional extra copy
3. `release/next` merged into `main` (regular merge, not squash)
4. `v1.1.0` tagged on `main`

## Try it yourself

```bash
# See branch structure
git log --oneline --graph --all --decorate

# Compare release notes range
git log v1.0.0..v1.1.0 --oneline

# See what is on release/next but not main (mid-week state)
git log main..release/next --oneline
```

## Release notes on GitHub

Open the [v1.1.0 release](https://github.com/isaac-gainline/release-branch-poc/releases/tag/v1.1.0) and view **What's Changed**. Compare range: `v1.0.0...v1.1.0`.

Each ticket PR merged into `release/next` appears as its own line when `release/next` is merged into `main`.
