# Khata — expenses, income, savings

A simple, colourful money app you can install on your phone. White background, five tabs, one-line entry. Everything is stored on your own device — no account, no server.

## The five tabs

**Daily** — one compact row: amount, category, date, note, Add. Entries stack up as a plain list grouped by day. Tap any row to edit or delete. Categories: groceries, food, transport, household, health, repair, education, gifts, personal, mobile, other.

**Monthly** — total expenses for the month (daily spending + monthly bills), the split between them, your fixed bills with a tick when paid, and a colour bar breakdown of where the money went. Bills like rent, utility, maid, internet, EMI and school fees are added once and come back every month; you can change one month's amount or skip a month.

**Income** — salary, investment, others. That's all three.

**Savings** — type the amount and name the account: FDR, DPS, or anything you write yourself (past names come back as suggestions). Shows what you saved this month, the all-time total, and a per-account balance.

**Balance** — income minus expenses, and nothing else. Savings sit apart and are never subtracted from this number; they're shown at the bottom only for reference.

Settings (gear, top right): currency symbol, optional carry-over of the balance to next month, backup/restore, CSV export, erase.

## Files

```
index.html              the whole app
manifest.webmanifest    name, colours, icons
sw.js                   offline cache
icons/icon-192.png
icons/icon-512.png
icons/maskable-512.png
```

## Putting it on GitHub Pages

1. Create a public repository, e.g. `khata`.
2. **Add file → Upload files**, drag in all four files plus the `icons` folder, commit.
3. **Settings → Pages** → Source: *Deploy from a branch*, branch `main`, folder `/ (root)`. Save.
4. Open `https://<your-username>.github.io/khata/` after a minute.

All paths are relative, so the repo subfolder URL works as is.

## Installing on your phone

- **Android / Chrome** — open the link → menu (⋮) → *Add to Home screen* → *Install*.
- **iPhone / Safari** — open the link → Share → *Add to Home Screen*. Must be Safari, not Chrome.

It then runs full screen and works with no internet.

## Good to know

- Data lives in the browser storage for that site. Clearing site data wipes it, so use **Settings → Save a backup file** now and then, and restore it on a new phone.
- It doesn't sync between devices — move data with a backup file.
- After you edit and re-upload `index.html`, bump `VERSION` in `sw.js` (e.g. `khata-v3`) so installed copies load the new version instead of the cached one.
