# MAKE WELCOME BOOK — FULL PROJECT HANDOFF (as of 2026-09-01)

Paste this into a new Claude session to continue with full context.
Working folder: ~/makewelcomebook (own git repo). Read PLAN.md there for the
complete decision log — this is the condensed operational picture.

## WHO / HOW TO WORK
- Owner: Mário Otruba (Slovakia, mario.otruba2003@gmail.com). NOT a developer —
  give him literal click-by-click steps for anything he must do himself;
  automate everything else. He gave Claude full A–Z authority; only money
  decisions, deletions and public posting need his OK.
- This venture is funded by his last savings (€250 budget). Spend carefully.
- SEPARATE project — never mix with STCKD, Reset Histamine or other ventures.

## THE PRODUCT
- makewelcomebook.com — browser-based welcome book generator for Airbnb/VRBO
  vacation-rental hosts. Host answers ~12 questions → gets print-ready welcome
  book + WiFi QR sign + house-rules/checkout pack. $29 one-time via Stripe.
- 62 designs (24 basic + 38 premium art incl. dark-luxury set), 3 formats
  (complete set / book only / one-page sign), drag-to-move text, fine-tune
  fonts/colors, "artwork on every page" toggle, auto-fit pages.
- Architecture: static site, NO backend. GitHub Pages from docs/ in repo
  github.com/molecoder22/makewelcomebook. Everything client-side; customer
  books live only in their browser localStorage. Print-CSS → PDF.
- Unlock: URL param. Stripe buyers → app.html?paid=MWB-UNLOCK-2026 (fires
  Google Ads conversion). Etsy buyers → app.html?paid=MWB-ETSY-2026 (no
  conversion event). Codes are client-side ⇒ inherently public; casual
  protection only. Tiled watermark on preview until unlocked.

## LIVE ACCOUNTS & IDS
- Domain: makewelcomebook.com @ GoDaddy (4×A GitHub Pages IPs, www CNAME
  molecoder22.github.io, MX mx1/mx2.improvmx.com, SPF improvmx).
- Email: *@makewelcomebook.com → mario.otruba2003@gmail.com via ImprovMX
  (catch-all, Active). hello@ is the public support address.
- Stripe: account "MakeWelcomeBook" (acct_1U7LLAEgS66qBLXy), product "Welcome
  Book Unlock" $29, payment link buy.stripe.com/9B6bJ15ypcBe0hReB36oo00,
  confirmation URL = the Stripe unlock link above. Statement descriptor
  MAKEWELCOMEBOOK / MWBOOK (was wrongly STCKD APP — fixed 8/28).
- Google Ads: account 917-571-4419, campaign WB-Search-Templates
  (id 24166614210). Google tag AW-18406718312; conversion label
  AW-18406718312/CvZwCL-C1uYcEOj2gMlE (fires once on Stripe unlock, $29).
- Microsoft Clarity: project y7j8xs7wx9 (recordings+heatmaps, Mario's IP
  87.197.89.172 excluded — re-add if his IP changes).
- Google Search Console: URL-prefix property https://makewelcomebook.com/,
  verified via meta tag DGiT9xLwGc2ZGHIzvMIWtdzmIsBRBSfOWMrPVwZc_Ns in BOTH
  index.html and app.html — DO NOT REMOVE. sitemap.xml submitted (5 URLs, OK).

## GOOGLE ADS CAMPAIGN STATE (2026-09-01)
- Search-only, Maximize Clicks, max CPC €2.80, budget €16/day (rarely spends
  >€8 — volume-capped, NOT budget-capped: lost-IS-budget = 0%).
- Geo: US (+50% bid adj), CA, AU. UK REMOVED 8/28 (73% of impressions, 0 sales,
  "guest book" = paper signing book in UK English — wrong intent).
- 39 exact-match keywords, 54 negatives, 2 RSAs (strength Average), 4 sitelinks
  ("See a Finished Example" brought a buyer), 6 callouts, structured snippet.
  AI Max OFF, broad match OFF, search partners OFF, presence-only targeting.
- RESULTS TO DATE: spend ≈ €35, 2 SALES (both ad-attributed, conversions=2 in
  UI): #1 Tarun Inuganti, Manhattan Beach CA, desktop, 8/28 — bought 81s in;
  #2 joyce@mostlymail.us 8/31, tablet (GoogleApp browser), the 42-min/139-click
  Clarity session. Net revenue ≈ €46.72 → PROFITABLE (~€12-17 depending on day).
  CVR ≈ 12.5%. Break-even ≈ CVR 6.8% at current CPCs.
- Expected daily volume post-UK-cut: only ~15-25 impressions/day, mostly during
  US daytime (= European evening). Low morning numbers are normal.
- KILL RULE still active: €120 total spend with zero sales → pause (moot now).
- OUTSTANDING (Mario only): Google advertiser verification (ID documents),
  Ads → Odporúčania → "Dokončenie overenia inzerenta". No deadline shown, but
  Google tightens identity checks; also blocks the in-account "confirm it's
  you" prompts that interrupt edits (unskippable after 9/1).

## FREE-TRAFFIC PLAN (research done 8/31)
Order: 1) Etsy (proven demand, $24.99 listing) 2) Pinterest (evergreen, 60-90d)
3) free WiFi-QR-sign tool page (SEO magnet — NOT built yet) 4) SEO articles
(GATED until sale #3 — currently 2/3) 5) Product Hunt after tool page
6) Reddit/FB groups only as genuine participation by Mario.
- LAUNCH KIT READY in ~/makewelcomebook/marketing/ (gitignored, repo public):
  etsy/Your-Welcome-Book-Access.pdf (delivery file w/ Etsy unlock link),
  etsy/1-main..6-onepage-sign.jpg (listing images), etsy/sample-book.pdf,
  pinterest/pin-01..38.jpg + pins.csv (titles/descriptions/links).
  Listing copy: ETSY-LISTING.md ($24.99, tags, SEO title).
- WAITING ON MARIO: create Etsy shop + Pinterest business account; then Claude
  uploads everything via his Chrome. Pinterest: publish 3-5 pins/day max.

## SITE STATE (all deployed & verified)
- Mobile: product-first hero, Edit/My-book bottom tabs, sticky CTA, 0 overflow.
- Landing: design gallery (24 covers), 7 CTAs, sticky mobile CTA (CSS-only).
- Builder: offer-on-intent dialog ($29 shown on Unlock/Download click; price
  stays visible in ads+landing — deliberate, don't hide it there), drag
  tutorial popup, debounced render + QR cache (INP fix), clean PDFs
  (@page margin 0), one-page sign shows ALL inputs, picker uses 160px thumbs.
- Tracking on both pages: gtag AW-18406718312 + Clarity y7j8xs7wx9.
- SEO hygiene: robots.txt, sitemap.xml, canonicals, OG tags + og.jpg, favicon.

## HARD RULES / GUARDRAILS
- NEVER "Airbnb" in brand/domain/ad text (trademark). Keyword use is fine.
- No fake sale pricing (never sold above $29 — "was $49" would be illegal
  reference pricing + Google misrepresentation risk).
- Legal: Mario operates without živnosť up to €2,200/yr revenue (his call,
  8/24). Track combined Stripe totals; warn well before the threshold.
- Refunds: 14-day money-back (terms/privacy/refunds pages live; hello@ works).
- Google Ads: never "Apply all" recommendations; harvest keyword ideas as
  EXACT match; keep AI Max / broad / partners OFF; mine search terms weekly.
- Etsy caveat: listing delivers a PDF containing the unlock link (grey-zone
  but common practice for tool access).

## IMMEDIATE NEXT STEPS
1. Mario: Etsy shop + Pinterest business account → Claude launches both kits.
2. Mario: Google advertiser verification (~30 min, ID needed).
3. Watch ads daily: with UK gone expect small-but-quality volume; if near-zero
   for 48h, investigate (identity deadline, billing).
4. At sale #3: start SEO articles + build free WiFi-sign tool page.
5. Re-check Clarity web vitals (INP was 780ms→fix shipped 8/31) and whether
   post-fix mobile visitors reach the builder (old baseline: 0 of 5 clicked).
