# MAKE WELCOME BOOK — FULL PROJECT HANDOFF (as of 2026-09-02, ~03:00 CEST)

Paste this into a new Claude session to continue exactly where the last one
stopped. Working folder: ~/makewelcomebook (own git repo, GitHub Pages from
docs/). Read PLAN.md there for the complete decision log — this file is the
condensed operational picture + the exact resume point.

## WHO / HOW TO WORK
- Owner: Mário Otruba (Slovakia, mario.otruba2003@gmail.com). NOT a developer —
  give literal click-by-click steps for anything he must do himself; automate
  everything else. Full A–Z authority given; only money, deletions and public
  posting need his OK (he has already approved: Etsy shop/listing edits, Google
  Ads edits, site deploys, Higgsfield generations).
- Budget: €250 total, his last savings. Spend carefully.
- SEPARATE venture — never mix with STCKD / Reset Histamine / TenderEulogy /
  LOCKD. cwd may be ~/stckd; always use absolute paths into ~/makewelcomebook.
- Claude drives Mario's Chrome via the claude-in-chrome extension (tabs_context_mcp
  createIfEmpty → navigate). He is logged in to: Google Ads, Etsy, Higgsfield,
  Gmail, ImprovMX, Stripe, Clarity, Search Console.
- Browser-pane (mcp__Claude_Browser) tabs pinned to file:// can't navigate; open
  live URLs with preview_start {url}.

## THE PRODUCT
- makewelcomebook.com — browser welcome-book generator for Airbnb/VRBO hosts.
  ~12 questions → print-ready welcome book + WiFi QR sign + one-page guest sign.
  $29 one-time via Stripe. 62 designs (24 basic + 38 premium art, 12 dark).
- Static site, NO backend, GitHub Pages from docs/ (repo molecoder22/
  makewelcomebook). Deploy = git push origin main (live in ~30-60 s).
- Unlock codes (client-side, casual protection): Stripe → app.html?paid=
  MWB-UNLOCK-2026 (fires Google Ads conversion); Etsy → app.html?paid=
  MWB-ETSY-2026 (NO conversion event).
- NEW 2026-09-02: docs/wifi-sign.html — FREE WiFi QR sign generator (SEO
  magnet + upsell). Live, in sitemap, linked from index.html footer. Verified:
  inputs → live preview, QR renders, print CSS, no console errors. Tracks
  gtag event wifi_sign_print. 12 designs, localStorage key mwb_wifisign.

## LIVE ACCOUNTS & IDS
- Domain makewelcomebook.com @ GoDaddy; email *@makewelcomebook.com →
  mario.otruba2003@gmail.com via ImprovMX (catch-all). hello@ is public support.
  NOTE: forwarded mail (Etsy codes etc.) lands in Gmail SPAM — if a code is
  missing, read it from app.improvmx.com → domain → Logs (subject shows code).
- Stripe acct_1U7LLAEgS66qBLXy, payment link buy.stripe.com/9B6bJ15ypcBe0hReB36oo00,
  descriptor MAKEWELCOMEBOOK. 3 payments total (Mario test 8/24, Tarun 8/28,
  Joyce 8/31). Net ≈ €23.36/sale.
- Google Ads 917-571-4419, campaign WB-Search-Templates id 24166614210
  (the account ALSO contains a "TenderEulogy Search" campaign from another
  venture — always filter by campaignId=24166614210; account-level totals mix
  both). Tag AW-18406718312, conversion label AW-18406718312/CvZwCL-C1uYcEOj2gMlE.
- Clarity y7j8xs7wx9 (Mario's IP 87.197.89.172 excluded).
- Search Console URL-prefix https://makewelcomebook.com/ (meta tag in index+app,
  DO NOT REMOVE). Sitemap has 6 URLs incl. wifi-sign.html.
- ETSY (live since 2026-09-02): shop https://www.etsy.com/shop/MakeWelcomeBook,
  listing https://www.etsy.com/listing/4566989528 . Registered with
  hello@makewelcomebook.com. Shop: W icon, photo banner, tagline, Slovakia,
  About story. Listing: title "Airbnb Welcome Book Template Alternative |
  Answer 12 Questions, Get a Finished Book + WiFi QR Sign | No Canva, 62
  Designs, VRBO Guest Guide", PRICE $29.00 (raised from $24.99 on purpose — a
  30% sale is to be applied, see RESUME), qty 999, Digital, category
  Templates, AI-generator disclosure ticked, 13 tags (airbnb welcome book,
  welcome book, airbnb host, vacation rental, house manual, airbnb template,
  guest book, airbnb signs, wifi sign, welcome guide, vrbo welcome book,
  airbnb guidebook, guest guide), description updated with design styles +
  "message within 14 days for refund". Files delivered: Your-Welcome-Book-
  Access.pdf + sample-book.pdf. 8 photos: 4 Higgsfield product photos (marble
  counter = main, book+framed sign, framed sign on console, bedroom) + light/
  dark cover grids + what-you-get + typographic headline.
  Etsy shows EU viewers price incl. VAT (e.g. $29 → ~$35.7); US see $29.
- Higgsfield: Mario's account (Google SSO, his gmail), model Nano Banana Pro,
  4 credits per 4K image. Upload our cover/sign as reference so the model
  renders OUR product. It garbles small text → composite the real sign with
  scratchpad composite_sign2.py (perspective warp + polynomial lighting).
  Originals in marketing/etsy/hf-4k/. First run may be falsely flagged NSFW
  (credits refunded) — just retry. Always verify the reference thumbnail in
  the prompt bar before generating.

## GOOGLE ADS — CURRENT SETTINGS
Search-only, Maximize Clicks, max CPC €2.80, budget €16/day (never binding),
geo US (+50% bid adj) + CA + AU (UK removed 8/28 — "guest book" = paper
signing book in UK English), presence-only, AI Max / broad / partners OFF,
39 exact keywords + 11 PHRASE keywords added 2026-09-02 ("welcome book
template", "airbnb welcome book", "vacation rental welcome book", "airbnb house
manual", "house manual template", "guest information book", "airbnb welcome
guide", "rental welcome book", "welcome book for vacation rental", "airbnb
guest guide", "short term rental welcome book"), 54 negatives, 2 RSAs
(strength Average), 4 sitelinks, 6 callouts, structured snippet.
Advertiser verification still OUTSTANDING (Mario only, needs ID).

## GOOGLE ADS AUDIT DATA (pulled 2026-09-02, all-time Aug 23 – Sep 2) — USE THIS, DON'T RE-PULL
Campaign: 429 impr · 24 clicks · CTR 5.59% · €54.66 · avg CPC €2.28 ·
2 conv · CVR 8.33% · CPA €27.33. Search IS 35.1%, lost to RANK 62.4%, lost to
budget 2.6%. Exact-match IS 35.1%.
Keywords with clicks (impr/clicks/cost/conv):
  [vacation rental guest book] 57/5/€9.67/0 — LOW QUALITY SCORE flag
  [guest welcome book] 188/5/€9.11/0
  [vacation rental welcome book template] 25/4/€10.36/1  ← converter
  [guest information book] 74/3/€6.63/0
  [short term rental welcome book template] 15/2/€6.91/0
  [vacation rental guest book template] 1/1/€2.00/0
  "guest information book" (phrase) 18/1/€2.76/0
  "rental welcome book" (phrase) 4/1/€2.78/0
  [guest welcome book template] 32/1/€2.48/0
  [vacation rental house manual] 2/1/€1.96/1  ← converter
Search terms: converters = "welcome book template for vacation rental" and the
house-manual query. WASTE = every "guest book" query (guest book, short term
rental guest book, accommodation guest book/guestbook, bnb guest book, custom
guest book for vacation home, event guest book, guest book for home/holiday
home/guest house, a guest book…): ≈ €24 of €54.66 (44%) with 0 conversions.
"Other search terms" bucket (privacy-hidden): 14 clicks, €31.91, 1 conv.
Geo: US 193 impr/14 clicks/€37.03/2 conv (CVR 14.3%, CPA €18.52); CA 35/1/
€2.48/0; AU 27/1/€2.52/0.
Device: Desktop 107/11/€28.27/1 conv (CVR 9.1%); Mobile 315/11/€21.66/0 conv;
Tablet 7/2/€4.73/1 conv.
Auction insights (impression share): etsy.com 43.6%, us 35.9%, amazon.com
17.9%, papier.com 15.6%, artifactuprising.com 11.2%, amazon.co.uk 11.2%,
zazzle, tabellara.com, hostgreeter.com, stayperk.com (<10%). Etsy/Amazon/
Papier/Artifact Uprising = physical guest-book sellers → confirms the
guest-book intent mismatch.
Keyword Planner US monthly volumes (12-mo avg, YoY): airbnb welcome book 390
(-46%), airbnb welcome book template 260 (-64%), airbnb signs 390, airbnb
guest book 260, vacation rental guest book 210, airbnb house manual template
140, airbnb house manual 90, airbnb guidebook template 70, airbnb welcome
guide 70 (+29%), airbnb welcome letter 70, airbnb wifi sign 50, welcome book
for airbnb 50, vacation rental welcome book 40, guest welcome book 40, airbnb
guest guide 20, digital welcome book airbnb 20, airbnb house rules sign 20,
short term rental welcome book 10, vrbo welcome book 10. Top-of-page bids
€0.5–1.0 low / €4–9.5 high. Competition "High" everywhere.
→ Relevant US demand ≈ 1,200–1,400 searches/month. Even at 100% impression
share and 6% CTR that is ~75 clicks/month ≈ 6 sales ≈ €140 net/month. GOOGLE
SEARCH ALONE CANNOT REACH €1,000/MONTH. Volume is the ceiling, not budget.

## ETSY RESEARCH (2026-09-02)
Search "airbnb welcome book template": our listing already shows on PAGE 1
(new-listing boost). Competitors: Canva templates at $2.45–$18 shown as
"sale" prices off fake $10–55 references; bundles (500+ items) $18; a few
"interactive/mobile" guides $21–28. Related searches: canva / lake cabin /
cabin / beach variants. We are the most expensive item on the page and the
only non-Canva "finished result". Decision: list at real price $29 (our own
site price = legitimate reference) and run a 30% Etsy sale → $20.30, still
premium but inside the page's price band. NO fake reference prices ever.

## RESUME POINT — UPDATED 2026-09-02 (late): ALL TASKS DONE, NOW PASSIVE
Everything from the previous resume list is COMPLETE and verified:
1. ✅ Etsy sale LAUNCH30: 30 % off, Everywhere, whole shop, 2 Sep – 1 Oct 2026.
   Public listing verified: $29 → $20.30 for US buyers (Mario's Slovak view
   shows $24.97 struck from $35.67 — same price with display VAT).
2. ✅ Mobile bid adjustment −50 % on campaign 24166614210 (verified in the
   Zariadenia table). The Zvýšiť/Znížiť control is a Material button-menu, not
   a <select>: click the button, then click the SECOND tiny item in the popup.
3. ✅ Campaign negatives "guest book" + "guestbook" (phrase), 54 → 56.
   ✅ Paused [vacation rental guest book] and [vacation rental guest book
   template] (both show "Pozastavené"). Max Clicks, €2.80 cap, US +50 %,
   CA/AU, €16/day, AI Max/broad/partners OFF — all unchanged.
4. ✅ ADS-AUDIT-2026-09-02.md written (repo root).
5. ✅ Etsy optimization complete (title/price/tags/description/photos/sale).
6. ✅ REALITY-CHECK-1000-EUR.md written (repo root).
7. ✅ PLAN.md updated, committed, pushed.

### CURRENT MODE: PASSIVE (Mario's instruction, a few days)
Daily checks ONLY, no changes unless something breaks:
 * Google Ads → campaign 24166614210 with date range "Včera" (Google's default
   ranges hide today and yesterday, which is why Mario has seen zeros before).
 * Stripe payments (3 so far: Mario's own test 8/24, Tarun 8/28, Joyce 8/31).
 * Etsy Stats: views / favorites / orders; Etsy Messages for buyer questions.
 * Clarity y7j8xs7wx9 for sessions and JS errors.
NEXT ACTIVE TASK when Mario says go: mine the Ads search-terms report (~4–5
Sep) for junk let in by the 11 phrase-match keywords, and add negatives.
WATCH: post-cleanup CPA — target ≈ €15. Kill criterion: another €40 of spend
with 0 sales → pause the campaign.
IF A SALE LANDS: message the buyer politely and ask for a review (Etsy) — the
first ten reviews are the single highest-leverage thing in the venture.

## HARD RULES / GUARDRAILS
- NEVER "Airbnb" in brand/domain/ad text (trademark). Keyword/descriptive use
  fine (Etsy title uses it descriptively like every competitor).
- No fake sale pricing: reference price must be a real price we sell at ($29).
- Legal: Mario operates without živnosť up to €2,200/yr revenue (his call
  8/24). Track combined Stripe+Etsy totals; warn well before the threshold.
- Refunds: 14-day money-back (site pages live; Etsy locked to "no returns"
  preset but we honor refunds manually via Etsy if messaged).
- Google Ads: never "Apply all" recommendations; harvest keyword ideas as
  EXACT/PHRASE manually; keep AI Max / broad / partners OFF; kill rule
  (€120 spend, 0 sales) is moot now.
- Etsy delivers a PDF containing the unlock link (grey-zone but common); the
  sample-book.pdf is included so the download is a real deliverable.

## FILES
- PLAN.md — full decision log (long); ADS-CAMPAIGN.md, ETSY-LISTING.md,
  DO-THIS-MARIO.md, HIGGSFIELD-PROMPTS.md.
- marketing/etsy/ (gitignored): 1-main.jpg … 8-headline.jpg (live set),
  src-cover.jpg, src-sign.jpg, hf-4k/ originals, v1/ old images,
  shop-icon.png, shop-banner.jpg, Your-Welcome-Book-Access.pdf, sample-book.pdf.
- marketing/pinterest/ pins 01–38 + pins.csv (shelved).
- Scratchpad scripts (may be gone with the session): build_etsy_assets.py,
  composite_sign2.py — logic described in PLAN.md if they need recreating.

## OUTSTANDING FOR MARIO (cannot be delegated)
1. Google advertiser verification (~30 min, ID).
2. Živnosť decision with accountant before scaling.
3. Optional: Microsoft Ads account (desktop-heavy, cheaper CPCs) if he wants
   another paid channel.
