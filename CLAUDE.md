# Make Welcome Book

Standalone venture — NOT related to STCKD or Reset Histamine. Work on it from
this folder (`~/makewelcomebook`), not from `~/stckd`.

Everything about this project — what it is, status, economics, kill rules,
Google Ads campaign details, division of labor — lives in **PLAN.md**. Read it
first. Campaign spec: ADS-CAMPAIGN.md. Mario's step-by-step guide:
DO-THIS-MARIO.md.

Key facts:
- Product: makewelcomebook.com — browser welcome-book generator for vacation
  rental hosts, $29 one-time via Stripe Payment Link. Static site in `docs/`,
  deployed on GitHub Pages (repo molecoder22/makewelcomebook), no backend.
- Google Ads: account 917-571-4419, campaign WB-Search-Templates
  (id 24166614210). Google tag AW-18406718312.
- Mario is not a developer: give literal click-by-click steps for anything he
  must do himself; automate everything else. He has full-autonomy preference —
  only money, deletions, and public posting need his OK.
- Never use "Airbnb" in brand or ad text (trademark); keyword use is fine.
- Legal: Mario operates without živnosť up to €2,200/year revenue (his call,
  2026-08-24). Track Stripe totals and warn before the threshold.
- Kill rule: €120 ad spend with zero sales → pause everything.

Local preview: `.claude/launch.json` serves `docs/` on port 4173.
