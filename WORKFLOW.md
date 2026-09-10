# Rollout 2026-09-18

**Production:** `main` at `v1.1.1`  
**Release branch:** `release/2026-09-18`  
**Target tag:** `v1.2.0`

## Rules

1. Branch each ticket from **`main`**
2. Before merging into `release/2026-09-18`, merge **`main` into your ticket branch**
3. PR base is **`release/2026-09-18`** (not `main`)
4. Rollout day: merge `release/2026-09-18` → `main`, then tag

## Ticket PRs (branch from main)

| PR | Ticket | Status |
|----|--------|--------|
| #11 | SES-3001: Waitlist confirmation email copy | Open |
| #12 | SES-3005: Checkout postcode validation | Open |
| #13 | SES-3010: Invoice PDF footer | Open |

After all tickets are merged, open PR `release/2026-09-18` → `main`.
