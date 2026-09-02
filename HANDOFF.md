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

## RESUME POINT — EXACTLY WHERE THE LAST SESSION STOPPED
The session ended mid-task (rate limit). Two dialogs were left open in Chrome
and will be gone; redo them:
1. ETSY SALE (not created yet): Shop Manager → Marketing → Sales and discounts
   → "Run a sale" → Set up. Percentage off = 30, Everywhere, duration 30 days
   from today, sale name e.g. LAUNCH30, apply to the single listing. Verify the
   public listing shows $20.30 (US) / strike-through $29.
2. GOOGLE ADS MOBILE BID ADJUSTMENT (not saved): campaign → Štatistiky a
   reporty → "Kedy a kde sa reklamy zobrazili" → Zariadenia tab (URL
   ads.google.com/aw/devices?ocid=8492560045&campaignId=24166614210) → Mobily
   row → Úprava ponuky cell → set DECREASE (Znížiť) 50% → Uložiť. The
   Zvýšiť/Znížiť dropdown resisted keyboard + ref clicks; try clicking the
   visible option in the opened menu, or use Google Ads Editor. Rationale:
   mobile = 315 impr/11 clicks/€21.66/0 conv all-time.
3. GOOGLE ADS OPTIMIZATIONS STILL TO APPLY (decided, not done):
   a. Add campaign negatives: phrase "guest book", "guestbook" (kills the 44%
      waste; keep [guest information book] and "guest welcome book" — they don't
      contain the contiguous phrase).
   b. Pause keywords [vacation rental guest book] (low QS, 0 conv), [vacation
      rental guest book template], and consider pausing [guest welcome book]
      (188 impr, 1.76% CTR, 0 conv) — or leave one week under the new negatives.
   c. Keep Max Clicks (only 2 conv — too few for Max Conversions). Keep €2.80
      cap; US +50%. Keep CA/AU (negligible spend).
   d. Mine search terms again ~Sep 4–5 (phrase match will add junk).
4. WRITE THE GOOGLE ADS AUDIT REPORT for Mario (he asked: "can we scale, does
   it make sense"). Use the data above. Conclusion: campaign is profitable but
   capped by ~1.3k US searches/month; realistic optimized Google ceiling ≈ 5–8
   sales/month (~€120–190 net); the "guest book" cleanup should cut CPA from
   €27 toward ~€15. Deliver as a readable report (markdown in repo, e.g.
   ADS-AUDIT-2026-09-02.md, or an Artifact page) + chat summary.
5. ETSY OPTIMIZATION STATUS: title/price/tags/description DONE and published;
   sale pending (item 1). Optional: second listing later (WiFi sign + book
   bundle framing), FAQs/shop link skipped (Etsy widgets rejected input).
   Pictures are final unless Mario objects.
6. ANSWER MARIO'S QUESTION "can this make €1,000 profit/month?" honestly:
   needs ~43 sales/month at €23.36 net (fewer if price/AOV rises). Google
   Search max ≈ 6–8/mo. Etsy at maturity in this niche: plausible 15–40/mo
   after reviews accumulate (top competitors have 4.6k–8k reviews; takes
   months). Plus Pinterest (shelved by Mario), SEO articles (start at sale #3),
   free WiFi-sign tool traffic, Bing Ads (needs his account), multi-property
   tier ($49). Verdict: €1k/month is possible but only as a multi-channel,
   3–6 month build, with Etsy as the main engine; not from Google Ads alone.
   Also: €1k/month blows past his €2,200/year no-živnosť ceiling in ~2.5
   months — he must settle the živnosť question with his accountant first.
7. THEN: Mario said "when all done I check, we let it be passive for a few
   days, then decide what next". So after 1–6: update PLAN.md, commit, give him
   the summary, and stop. Daily passive checks only (Ads today/yesterday via
   the "Včera" date range, Stripe payments, Etsy stats, Clarity).

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
