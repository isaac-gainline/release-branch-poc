# Rollout workflow: release/2026-09-25

Target tag: **v1.3.0**

## Rules

1. Ticket branches are created from **`main`**, not from the release branch.
2. Before merging a ticket PR into this release branch, merge **`main`** into the ticket (hotfixes on main).
3. After another ticket has merged here, merge **`release/2026-09-25`** into your ticket branch (or use **Update branch** on GitHub) to resolve conflicts in shared files.
4. Use **Create a merge commit** when merging ticket PRs (not squash).
5. Rollout day: if `main` moved, merge **`main` → release** once, then **`release` → `main`**.

## Shared conflict surfaces (this exercise)

| File | Why it conflicts |
|------|------------------|
| `src/features.json` | Multiple tickets flip different feature flags in one JSON file |
| `resources/copy/checkout.yaml` | Competing checkout headlines and subtitles |
| `config/rollout.php` | Different `copy_bundle` values per ticket |

## Suggested merge order

| Order | Ticket | PR |
|-------|--------|-----|
| 1 | SES-3101 Club portal login | First merge (clean) |
| 2 | SES-3105 Basket summary | Conflicts until synced with release |
| 3 | SES-3110 Email footer legal | Conflicts on `features.json` |
| 4 | SES-3112 Checkout step labels | Conflicts on copy + config |

## Practice scenario

All four PRs were opened from the same `main` tip **without** merging the release branch into each ticket. Only the first PR should merge cleanly. The others should show **This branch has conflicts that must be resolved** until you merge `release/2026-09-25` into the ticket branch.
