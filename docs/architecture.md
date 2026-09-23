# AlwaysConnected architecture

v0 public map. This document is safe to publish. It describes layers and boundaries, not credentials or runnable payout code.

## Purpose

AlwaysConnected is a control surface for three jobs:

1. Keep people and systems reachable.
2. Keep automation visible (what ran, what failed, what is waiting).
3. Keep business infrastructure cheap to launch (GitHub + Pages first).

## Layers

```
Public surface — this site, GitHub Pages, docs
Control plane (private) — agent board, job ledger, human gates
Execution (private / local) — Termux, Replit, scheduled runners
Money movement — official processors only; keys never in git
```

## What belongs in this repository

- Brand and product copy
- Static site
- Architecture notes
- Issue templates later

## What never belongs in this repository

- Passwords, PATs, session cookies
- Stripe / Plaid / PayPal secret keys
- Customer PII
- Scripts that move money without a human-reviewed, legal processor path
- Anything that would still be dangerous if the repo is public (it is)

## GitHub Pages path

Source of truth: `main` branch, site root.

Expected URL after Pages is enabled:

`https://huntermyers103121-png.github.io/AlwaysConnected/`

Custom domains can wait. v0 does not need one.

## Next private systems (not built in this commit)

- Job ledger with idempotent task IDs
- Agent runner with explicit allow-lists
- Status heartbeats
- Human approval step before any external side effect
