[README.md](https://github.com/user-attachments/files/30289061/README.md)
# Cover Pro Painting — Exterior Estimator

Internal field tool for Cover Pro Painting sales estimators. Enter measurements, select prep level and paint system, get a consistent locked-math estimate in minutes. Not customer-facing.

**Live app:** hosted via GitHub Pages from this repo (Settings → Pages for the URL).

## How it works

- The entire app is one file: `index.html`. No build tools, no dependencies to install.
- Estimators open the live URL on their phone (Add to Home Screen makes it an app icon).
- All pricing math is locked — estimators enter measurements and selections only.
- Estimate history saves per-device (last 10) in the browser.
- Two copy modes: **Customer copy** (rolled-up totals, safe for proposals) and **Internal copy** (full math — never send to customers).

## Updating prices

1. Open `index.html` in this repo → click the pencil icon.
2. All pricing constants are in the first ~35 lines, labeled in plain English:
   - `PREP_RATES` — the three prep tiers (`rate:` is the $/sq ft)
   - `TRIM_RATE` — $/linear ft for trim
   - `STORY_ADJ` — story adjustment percentages
   - `PAINTS` — paint systems and `costPerGal`
   - `DOOR_PRICE` — per-door add-on price
3. Change numbers only. Don't touch commas, quotes, or brackets.
4. Commit changes. Live for everyone in about a minute — no redeploy needed.

For anything beyond number swaps (adding/removing fields or features), edit carefully or rebuild the file — structural changes can break the app if a bracket goes missing.

## Version history

- **V1.1** — Removed house sq ft field. Story adjustment simplified: 1–2 story +0%, 3 story +10%. Prep rates updated.
- **V1.0** — Initial launch. Body + trim pricing, prep tiers, story adjustment, paint upgrades, door and custom add-ons, per-device history, dual copy modes.

## V2 wishlist (parked)

- DripJobs sync for customer info
- Company-wide estimate history (needs a backend)
- Architecture complexity tiers (needs multipliers defined)
- Production outputs: labor hours, crew size, days (needs production rates defined)
