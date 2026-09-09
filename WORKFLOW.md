# Rollout 2 walkthrough

This repo is set up at **mid-week** in the second rollout cycle.

**Previous release:** `v1.1.0` on `main`
**Target release:** `v1.2.0`

## Current state

| Branch | Status |
|--------|--------|
| `main` | Production at `v1.1.0` |
| `release/next` | Reset from `main`. SES-2849 merged |
| `SES-2861-membership-basket` | Open PR waiting to merge |
| `SES-2901-renewal-reminder` | Branch ready (PR not yet opened) |

## Step 1: Merge tickets into release/next

1. Merge [PR #8](https://github.com/isaac-gainline/release-branch-poc/pull/8) SES-2861 (merge commit, not squash)
2. Open and merge PR for SES-2901 into `release/next`

## Step 2: Merge release/next into main

1. Create PR: base `main`, compare `release/next`
2. Title: `Rollout: merge release/next into main`
3. Merge with **Create a merge commit** (not squash)

## Step 3: Tag v1.2.0

1. Update `VERSION` to `1.2.0` on `main`
2. Create tag `v1.2.0` on `main`
3. GitHub → Releases → **Generate release notes**
4. Compare range: `v1.1.0...v1.2.0`

Ticket PRs (#7, #8, #9) should each appear as their own line.

## Rules

- One PR per ticket into `release/next`
- PR title: `SES-1234: Short summary`
- Merge `release/next` → `main` without squashing the whole branch
