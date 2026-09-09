# Rollout workflow walkthrough

This repo is set up at **mid-week** in a rollout cycle.

## Current state

| Branch | Status |
|--------|--------|
| `main` | Production baseline (`VERSION` = 1.0.0). Tag: `v1.0.0` |
| `release/next` | Has SES-1380 and SES-1392 merged |
| `SES-1400-upsells-copy-v2` | Open PR #5 waiting to merge |

## Step 1: Merge the last ticket into release/next

1. Open [PR #5](https://github.com/isaac-gainline/release-branch-poc/pull/5)
2. Merge with **Create a merge commit** (not squash)
3. Confirm `release/next` now has all three feature flags enabled in `src/features.json`

## Step 2: Merge release/next into main

1. Create a PR: base `main`, compare `release/next`
2. Title: `Rollout: merge release/next into main`
3. Merge with **Create a merge commit** (not squash)

## Step 3: Tag and release

1. Update `VERSION` to `1.1.0` on `main` (optional separate commit)
2. Create tag `v1.1.0` on `main`
3. GitHub → Releases → **Draft a new release**
4. Choose tag `v1.1.0`, click **Generate release notes**
5. Compare range should be `v1.0.0...v1.1.0`

Each ticket PR (#1, #4, #5) should appear as its own line in What's Changed.

## Commands (local clone)

```bash
git clone https://github.com/isaac-gainline/release-branch-poc.git
cd release-branch-poc

# Mid-week: what is on release/next but not main?
git fetch origin
git log origin/main..origin/release/next --oneline

# After rollout: release notes range
git log v1.0.0..v1.1.0 --oneline

# Branch graph
git log --oneline --graph --all --decorate -20
```

## Rules (same as production)

- One PR per ticket into `release/next`
- PR title: `SES-1234: Short summary`
- Never point UAT at `release/next`
- Merge `release/next` → `main` without squashing the whole branch
- Hotfixes still go to `main` directly
