# Rollout 2026-09-18

**Production:** `main` at `v1.1.1`  
**Release branch:** `release/2026-09-18`  
**Target tag:** `v1.2.0`

## Rules

1. Branch each ticket from **`main`**
2. Before merging into `release/2026-09-18`, merge **`main` into your ticket branch`** (hotfixes on `main`)
3. PR base is **`release/2026-09-18`** (not `main`)
4. Rollout day: if `main` moved after the last ticket merge, merge `main` → `release/2026-09-18`, then PR to `main`
5. Tag `v1.2.0` on `main` after rollout merge

## Ticket PRs (all branch from `main`)

| PR | Ticket | Status |
|----|--------|--------|
| [#11](https://github.com/isaac-gainline/release-branch-poc/pull/11) | SES-3001: Waitlist confirmation email copy | Open |
| [#12](https://github.com/isaac-gainline/release-branch-poc/pull/12) | SES-3005: Checkout postcode validation | Open |
| [#13](https://github.com/isaac-gainline/release-branch-poc/pull/13) | SES-3010: Invoice PDF footer | Open |

Merge with **Create a merge commit** (not squash).

After all tickets are on `release/2026-09-18`, open PR **`release/2026-09-18` → `main`**.
