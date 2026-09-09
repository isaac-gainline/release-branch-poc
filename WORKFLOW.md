# Rollout 2 walkthrough

**Previous release:** `v1.1.0` on `main`  
**Target release:** `v1.2.0`

## Current state (mid-week)

| Branch | Status |
|--------|--------|
| `main` | Production at `v1.1.0` |
| `release/next` | Reset from `main`. SES-2849 merged |
| `SES-2861-membership-basket` | [PR #8](https://github.com/isaac-gainline/release-branch-poc/pull/8) open |
| `SES-2901-renewal-reminder-v2` | [PR #9](https://github.com/isaac-gainline/release-branch-poc/pull/9) open |

## Your steps

### 1. Merge tickets into `release/next`

1. Merge [PR #8](https://github.com/isaac-gainline/release-branch-poc/pull/8) SES-2861 — **Create a merge commit**
2. Merge [PR #9](https://github.com/isaac-gainline/release-branch-poc/pull/9) SES-2901 — **Create a merge commit**

(PR [#7](https://github.com/isaac-gainline/release-branch-poc/pull/7) SES-2849 is already merged.)

### 2. Merge `release/next` into `main`

1. New PR: base `main`, compare `release/next`
2. Title: `Rollout: merge release/next into main`
3. **Create a merge commit** (not squash)

### 3. Tag `v1.2.0`

1. Update `VERSION` to `1.2.0` on `main`
2. Create tag `v1.2.0` on `main`
3. Releases → **Generate release notes**
4. Compare range: `v1.1.0...v1.2.0`

PRs #7, #8, #9 and the rollout merge PR should each appear in What's Changed.
