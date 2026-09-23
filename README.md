# AlwaysConnected

AI-powered connectivity, automation, and business infrastructure.

**Repository:** [huntermyers103121-png/AlwaysConnected](https://github.com/huntermyers103121-png/AlwaysConnected)

**Public site (GitHub Pages, after you enable it):**  
https://huntermyers103121-png.github.io/AlwaysConnected/

This is the first public surface for AlwaysConnected — a control layer for keeping people, systems, and money-movement workflows connected without buying hosting or a domain up front.

## What this repo is

| Layer | Purpose |
| --- | --- |
| Public site | Brand, product story, system map |
| `/docs` | Architecture notes for the live system |
| GitHub Pages | Free hosting from the `main` branch |

Later layers (agent control board, job ledger, payouts, local/Termux runners) stay out of the public site until they are ready and legal to expose.

## Enable GitHub Pages (required once)

1. Open [repository Settings → Pages](https://github.com/huntermyers103121-png/AlwaysConnected/settings/pages)
2. **Source:** Deploy from a branch
3. **Branch:** `main`
4. **Folder:** `/ (root)`
5. Save

GitHub usually publishes within 1–2 minutes.

Live URL:

```
https://huntermyers103121-png.github.io/AlwaysConnected/
```

No custom domain is required for v0.

## Local preview

Open `index.html` in a browser, or from this folder:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## File map

```
/
├── index.html          Public landing page
├── styles.css          Theme and layout
├── app.js              Nav, clock, status chips
├── docs/
│   └── architecture.md System layers
└── README.md
```

## Status

- v0 — public brand + architecture map
- No backend, no secrets, no payment keys in this repo
- Do not commit `.env`, API keys, Stripe/Plaid secrets, or tokens
