# Make Welcome Book — Master Plan

**Decided 2026-08-22.** New digital product venture. Budget: €250 total (Mario's last savings — spend like it's the last money on earth, because it is). Claude has A–Z decision authority; Mario does only what Claude cannot (payments, accounts).

## The product

**makewelcomebook.com** (domain verified available via RDAP 2026-08-22, ~€12 to register).

A web-based **welcome book generator** for Airbnb / VRBO / vacation-rental hosts:
host answers ~12 simple questions (WiFi, check-in steps, house rules, appliance
notes, local tips, emergency info) → instantly receives a finished, beautifully
designed welcome book. No Canva, no design skills, no subscription.

**Deliverables the customer gets (all generated in the browser, no backend):**
- Welcome book as print-ready PDF (multiple theme designs)
- WiFi QR-code sign (scan to connect)
- Printable pack: house rules sign, check-out card, review-request card
- Free re-edits (their answers stay in their browser)

**Price:** $29 one-time (anchor $49). Launch sale framing allowed, honest.

## Why this product (research summary)

- Etsy proof of demand: top "airbnb welcome book template" listings have **8,000**
  and **4,600 reviews** → tens of thousands of real buyers.
- Etsy is a race to the bottom (€2–15 DIY Canva templates) → we do NOT sell a
  template; we sell the finished result.
- SaaS competitors (Touchstay ~$99/yr, Hostfully) are subscriptions → we are the
  one-time-payment middle of the market. That gap is empty.
- Buyer = small business owner (has money, values time), searches with intent
  ("airbnb welcome book template"), low-competition long-tail keywords.
- No health/finance ad-policy problems. Rejected alternatives: wedding speeches
  (killed by free AI generators), digital planners / Notion templates
  (saturated, buyers browse Etsy not Google).

## Trademark care

- Brand/domain/logo NEVER contains "Airbnb" (trademark). Brand is neutral:
  "Make Welcome Book", works for Airbnb, VRBO, Booking, any rental.
- Ad copy: prefer "vacation rental" / "welcome book"; "Airbnb" as a *keyword*
  is fine, in *ad text* may be blocked by Google trademark policy.
- On-page descriptive use ("works great for your Airbnb listing") is OK.

## Architecture (keep it dead simple)

- Static site, no backend. Hosting: Cloudflare Pages or Netlify (free) — reuse
  whatever stack resethistamine uses (see ~/resethistamine/HANDOFF.md).
- Flow: landing page → generator form (free, live preview, watermarked) →
  Stripe Payment Link ($29, reuse Mario's existing Stripe account) → success
  redirect unlocks full downloads. Answers persist in localStorage.
- PDF via print CSS; QR codes generated client-side (inline lib, no CDN).
- 3–5 book themes at launch.

## Channels

1. **Google Ads (€200 of budget):** exact-match long-tail — [airbnb welcome book
   template], [airbnb welcome book], [vacation rental welcome book], [airbnb
   house manual template], [welcome book for airbnb]. ~€10/day. Geo: US, UK, CA,
   AU. Verify real CPCs in Keyword Planner BEFORE first spend.
   **Kill rule: €120 spent with zero sales → pause everything, fix page, only
   then spend the rest.** Scale only from revenue.
2. **Etsy listing (free hedge, $0.20):** list the product on Etsy too at
   Etsy-market pricing — free marketplace traffic + reviews.
3. Free: Reddit r/airbnb_hosts etc. (honest, no spam), Pinterest pins of the
   book designs.

## Honest economics (told to Mario, he accepted the risk)

€200 ads ≈ 130–400 clicks at $0.5–1.5 CPC. At 1–3% conversion → roughly 2–10
sales ($58–290). First €250 is a TEST that buys data, not a jackpot. Profit
comes from scaling what the test proves + Etsy channel.

## Legal (same as Reset Histamine — not re-litigating, just tracking)

Selling here has the same open question as resethistamine.com: Mario has no
živnosť (trade licence) yet. ONE message to his accountant covers both stores.
Must be answered before ads go live.

## Division of labor

- Claude: everything buildable — research (done), product, site, copy, ad
  campaign design, Etsy listing text, monitoring plan.
- Mario (plain click-by-click steps only, when the time comes):
  1. Buy makewelcomebook.com (~€12) — when site is ready to deploy.
  2. Create Google Ads account + add his card himself (Claude must not enter
     payment credentials or create accounts).
  3. Approve the Stripe payment link creation in his Stripe dashboard.

## Status

- [x] Market research + product decision (2026-08-22)
- [x] Domain chosen & verified available
- [x] Build generator + landing page (2026-08-22, verified in browser)
- [x] Legal pages: terms/privacy/refunds (2026-08-22, trader identity mirrored
      from resethistamine)
- [x] Decision: NEW separate Google Ads account (Mario's choice 2026-08-22 —
      full separation from histamine account; he creates it when site is live)
- [x] Creative upgrade: 16 themes × distinct typography × 4 cover layouts;
      sample mode at app.html?sample=1 (2026-08-22, verified in browser)
- [x] Ads campaign spec written (ADS-CAMPAIGN.md), Etsy listing written
      (ETSY-LISTING.md), Mario's steps written (DO-THIS-MARIO.md)
- [x] Repo committed locally; site folder renamed site/ → docs/ for GitHub Pages
- [x] LIVE 2026-08-22: repo github.com/molecoder22/makewelcomebook, GitHub
      Pages from /docs, domain makewelcomebook.com bought by Mario, DNS set by
      Claude via Chrome extension (4×A + www CNAME), site verified 200 OK.
      HTTPS enforcement pending cert (background job running).
      NOTE: GoDaddy no longer has free email forwarding — plan: free ImprovMX
      (Mario signs up 1 min, Claude adds MX records). hello@ not receiving yet.
- [x] Stripe LIVE 2026-08-22: separate MakeWelcomeBook account (Mario created),
      product "Welcome Book Unlock" $29, payment link
      buy.stripe.com/9B6bJ15ypcBe0hReB36oo00 wired into site, activation clean
- [x] HTTPS live + enforced (Let's Encrypt, valid to 2026-11-20; "not secure"
      Mario saw was his browser's cached cert-bypass — fixed by Chrome restart)
- [x] Product expanded same day: 50 designs (26 Higgsfield premium free + 24
      basic, two-section picker), page formats (set/book/one-page sign),
      fine-tune fonts+colors, sticky follow-along preview, real-cover hero
- [x] Google Ads account created 2026-08-23: 917-571-4419 "MakeWelcomeBook"
      (old closed acct 624-317-1903 was the billing blocker; billing+identity
      done by Mario; advertiser name: Mário Otruba). Google tag: AW-18406718312
- [x] Campaign "WB-Search-Templates" BUILT & PAUSED (id 24166614210):
      Search-only, clicks bidding w/ €1.00 max CPC, €8/day, US+UK+CA+AU,
      English, 10 exact-match keywords, 1 RSA (8 headlines/4 descriptions),
      AI Max off. Google estimate: 43 clicks/wk @ €1.02 avg CPC.
- [x] LEGAL CALL (Mario, 2026-08-24): OK to operate up to €2,200/year revenue
      without živnosť — his decision, gate cleared by him.
- [x] ★ CAMPAIGN ACTIVATED 2026-08-24 ★ — 15 negative keywords added, AI Max
      confirmed fully off (review screen had shown stale info), base gtag
      AW-18406718312 installed on site, campaign ENABLED ("Eligible (limited)"
      — low-volume advisory normal for exact match). Ads serve after Google's
      standard ad review (~1 day).
- [x] Conversion wiring DONE 2026-08-24: Purchase action label
      AW-18406718312/CvZwCL-C1uYcEOj2gMlE fires once on ?paid= unlock ($29);
      tag verified live on site (gtag + dataLayer present)
- [x] Diagnostics cleanup 2026-08-24 (Mario: "no shorts"): keywords expanded to 25
      exact-match (some overlaps deduped by Google), RSA expanded 8→15 headlines
      (ad strength Poor→Average, recalculating after save), 4 sitelinks added
      (Example / Pricing / Start Free / WiFi QR — approved same day). Remaining
      "limited" status = normal low-search-volume advisory on exact match.
- [x] Playbook audit 2026-08-24 (Mario's "Google Ads Expert Brain" doc, A–Z):
      * Location targeting: default "Presence or interest" trap FIXED →
        Presence-only (US/UK/CA/AU) — biggest waste-cutter of the audit
      * Networks: search partners + display expansion verified OFF
      * Negatives 15→50 (broad, campaign level): bargain (cheap/discount/
        coupon/promo code/voucher), jobs (hiring/salary/career/careers/resume),
        info (how to make/how to write/wiki/wikipedia/reddit/definition/
        meaning/sample/samples/blog), wrong-audience (wedding/baby/classroom/
        teacher/school), platforms (youtube/facebook/amazon/ebay/canva),
        media (image/images/photo/photos), cheapest
      * 2nd RSA added to ad group (playbook: +6.6% conv from 2nd ad) —
        15 headlines/4 descriptions, different angle (done-for-you/no-Canva/
        one-time price), path /welcome-book/builder; deleted Google's
        auto-suggested duplicate sitelinks before saving
      * Callouts ×6 added: One-Time $29 Payment / 50 Designs Included /
        Instant PDF Download / 14-Day Money-Back / No Design Skills Needed /
        Free Re-Edits Forever
      * Structured snippet added (EN, header "Types"): Welcome Book, WiFi QR
        Sign, House Rules Sign, Check-Out Card, Review Card
      * Conversion action verified: Primary, data-driven attribution,
        per-transaction values (€1 fallback), 30-day click window,
        status "awaiting conversions" (≤48 h, normal)
      * Keyword-ideas harvest 2026-08-24 pm: Google's "add new keywords"
        recommendation (35 broad-match suggestions) NOT auto-applied — 13
        genuinely-new phrasings added as EXACT match instead (guest guide /
        guest welcome book / rental welcome book / welcome binder / vrbo
        template / short term rental template / pdf variants), rest were
        reorder-duplicates or blocked words (free/sample/examples). Now 38
        exact keywords. Recommendation dismissed, incl. the search-partners
        opt-in card (playbook: partners stay OFF). Never click "Apply all"
        on keyword recommendations — always harvest to exact manually.
      * Bidding decision: STAY on Max Clicks + €1.00 CPC cap for the
        early-data phase (playbook Stage-1 fit; cap protects $29-product
        economics). Switch to Maximize Conversions after first conversions /
        ~2 weeks of click data; tCPA only at 15–30 conv/30d — likely never
        at this scale, Max Conversions is the realistic ceiling.
      * Known gaps (accepted): no Enhanced Conversions (no email captured
        on-page at conversion; Stripe handles it), no Consent Mode v2 (not
        targeting EEA), no brand campaign yet (zero brand search volume).
- [ ] Monitor day 1/3/7: spend, CTR, search-terms report. KILL RULE ACTIVE:
      €120 spent with zero Stripe sales → pause everything.
      Day-3 data (Aug 23-26): 31 impr, 3 clicks, 9.7% CTR, €2.96 spent,
      0 conv. Search-term mining: added [guest information book] (2/2 clicks,
      100% CTR — buyer phrase we missed) as 39th keyword; blocked 4 waste
      terms ([guest feedback book],[guest sign book],[visitor book],
      [guest book for home visitors]) → 54 negatives. UK queries answering
      first (holiday home/let). Delivery was capped by €1.00 max CPC (avg
      CPC pinned at €0.99) → Mario authorized more spend 2026-08-26,
      max CPC raised €1.00 → €1.50. Budget stays €8/day, kill rule stays.
      ★ 3-DAY SPEED SPRINT (Mario, 2026-08-26 eve): budget €8 → €16/day AND
      max CPC €1.50 → €2.00, to buy data fast. Max exposure ~€48 over 3 days
      (still < €120 kill line). Impressions already 31→47 after the €1.50
      step. REVIEW DUE 2026-08-29: if spend approaches €60-70 with 0 sales,
      revert to €8/day + €1.50 and shift focus to landing-page conversion
      (Clarity recordings) rather than more traffic.
- [ ] Revenue watch: Mario's €2,200/year threshold — track Stripe totals
      (both stores) and warn well before crossing
- [x] DARK PREMIUM SET 2026-08-24 evening (Mario's request, Pinterest
      dark-luxury trend): 12 new Higgsfield art themes (27-38: noir gold,
      midnight botanical, dark floral, black marble, celestial, charcoal
      linen, dark academia, golden wave, ebony palm, chalkboard, dusk peaks,
      gold leaf) — 4K Nano Banana Pro, all QC'd first try. New dark:true
      theme flag: light cover text, dark one-page cards, white-backed QR
      (scannable on black). Now 62 designs / 38 premium. Same day: fixed
      basic-themes-masked-by-fine-tune bug, tiled screenshot-proof watermark,
      clean PDFs (@page margin 0), one-page sign shows ALL inputs.
      Mario confirmed real purchase flow works end to end.
- [x] FULL FUNNEL AUDIT 2026-08-24 night ("run only ads and nothing more"):
      walked ad->landing->builder->Stripe->unlock->download on mobile+desktop.
      FIXED: theme picker loaded all 38 full arts (4.3MB) -> 160px thumbs
      (101KB, 43x lighter); no favicon -> inline SVG W monogram both pages;
      no OG/social tags -> og:title/desc/image + og.jpg (3-cover composite);
      builder had NO legal links -> paybar now links Refunds/Terms/Privacy +
      "14-day money-back"; copy "book on the right" -> neutral (mobile);
      recompressed heaviest arts. VERIFIED: Stripe checkout clean ($29,
      Apple Pay), zero failed site resources, mobile layout single-column OK,
      landing mobile OK. Site is ads-ready hands-off.
      REMAINING (Mario): ImprovMX signup so hello@ actually receives mail —
      it's printed in terms/privacy/refunds; until then refund requests have
      no working channel (Stripe dispute risk).
- [x] ★ MOBILE OVERHAUL 2026-08-26 (Mario: "90% of views are mobile, it
      sucks on mobile"). Measured on 375px viewport, real bugs found+fixed:
      * 49px HORIZONTAL OVERFLOW (page 424px wide on 375px screen) — header
        and all copy were cut off. Cause: grid track min-width:auto +
        unwrappable header. Fix: minmax(0,1fr) + min-width:0 + wrapping header.
      * Preview was 3.1 SCREENS DOWN (form is 2740px tall) — ad visitors
        never saw the product. Fix: sticky bottom tab bar [✎ Edit][📖 My book],
        one tap to the live book; "My book" pulses when the book changes.
        Sample-data button auto-flips to the book.
      * Buy button was 34px CLIPPED behind the new tab bar → paybar lifted.
      * Tip popup covered the form on load and the book in preview → now
        compact, shows only in preview, dismisses on first drag.
      * CASCADE BUG: mobile rules sat before base rules and were being
        overridden → moved all mobile overrides to the END of the stylesheet.
      Verified: 0 overflow, book visible without scrolling, buy button clear,
      desktop unchanged (tabs hidden, two columns, paybar normal).
- [x] OFFER-ON-INTENT 2026-08-26 (Mario: let them build first, show price on
      click): persistent price banner in the builder replaced with a slim
      "Free to try — your book is saved as you type" + Unlock button
      (paybar 141px → 89px on mobile, more room for the book). Full offer now
      opens as a dialog on "Unlock my book" OR "Download PDF": $29 one-time,
      5 benefit bullets, 14-day money-back, Stripe + legal links.
      NOTE (deliberate, keeps us honest & Google-policy safe): price stays
      visible in the ad copy and on the landing page, so nobody reaches the
      builder without having seen $29 — this declutters the workspace, it is
      NOT hidden pricing. Do not remove $29 from ads/landing.
- [x] CLARITY VERIFIED 2026-08-27: tag live on BOTH pages (clarity.ms/tag/
      y7j8xs7wx9 + clarity.js loading, window.clarity = function), 56 sessions
      recorded, replays + AI session summaries working. Own IP 87.197.89.172
      excluded in Settings→IP blocking so our testing stops polluting data
      (re-add if Mario's IP changes; it is dynamic).
      ★ FIRST REAL AD-VISITOR BEHAVIOUR (referrer google.com, UK, MobileSafari
      /tablet): landed on the LANDING page, 14s and 38s, **0 clicks**, 1 page,
      left without reaching the builder. Sample is tiny (2-3 real visits) so
      it is a hint, not a verdict — but the drop-off is at the landing page,
      not the builder. Watch this on Saturday: if the pattern holds with
      20-35 clicks, fix the landing page (CTA prominence / intent mismatch:
      "template" searchers may expect a free Canva file), not the builder.
- [x] ★★★ FIRST REAL SALE 2026-08-28, 03:53 CEST ★★★
      Customer: Tarun Inuganti, Rancho Palos Verdes, California US (real
      stranger, paid via Stripe Link, risk level Normal, guest checkout).
      $29.00 USD → €24.89, Stripe fee €1.53, NET €23.36 (available Sep 2).
      Google Ads recorded the conversion (tracking works end-to-end).
      ECONOMICS Aug 23-28: spend €12.63 / 8 clicks / 97 impressions /
      CTR 8.25% / avg CPC €1.58 / 1 conversion / cost-per-sale €12.63.
      → PROFIT on first sale ≈ €10.73 (ROAS ~1.85x). Exact converting query
      hidden by Google (low-volume privacy threshold, shown only in the
      "other search terms" bucket: 4 clicks, €6.83, 25% CVR).
      BREAK-EVEN MATH: at €1.58 CPC we need ≥6.8% conversion rate to break
      even (14.8 clicks per sale = €23.36). Current 12.5% is above it but
      based on ONE sale — expect it to fall. Watch this number.
- [x] Stripe fix 2026-08-28: statement descriptor was "STCKD APP" (from the
      other venture) → customers' card statements now read MAKEWELCOMEBOOK
      (short: MWBOOK). Wrong descriptor = classic chargeback trigger.
      TODO next: Stripe product description still says "all 34 themes" (now 62).
- [x] BUYER SESSION WATCHED (Clarity, user hdsjwy, Aug 28 05:52, 08:30 min,
      57 clicks, 5 pages, US / Chrome / DESKTOP). What he actually did:
      arrived from Google → clicked "Build my welcome book" within seconds →
      started typing at 00:15 → **paid $29 at 01:21 (81 seconds in!)** →
      then spent ~5 min filling WiFi, contact, check-in, house rules, trash
      day, local tips → downloaded multiple PDFs at 06:55 and 07:04 →
      previewed page by page. Property: beach rental in Manhattan Beach CA,
      hosts Tarun & Sheela. Chose premium art design "Seaside" AND switched
      on the "artwork on every page" toggle (built the day before he bought).
      LESSONS: (1) offer-on-intent did not slow him down — serious hosts
      decide in ~80s; (2) the premium art section is what he used; (3) the
      product held up: he completed a full book and downloaded it twice.
      CONTRAST worth watching: every UK MOBILE visitor so far bounced in
      4-38s with 0 clicks, while the US DESKTOP visitor converted. If that
      pattern holds on Saturday, consider a device bid adjustment toward
      desktop and a separate look at the mobile landing page.
      NOTE: we cannot retrieve a customer's book — it lives only in their
      browser (localStorage, no backend). Clarity replay is the only view.
- [x] MOBILE LANDING FIXED 2026-08-28 (Mario's call: "0% of mobile converts,
      don't wait for a bigger sample"). Diagnosis: not speed (0.7s, 435KB) and
      not layout overflow (0px) — it was ORDER. Mobile got ~600px of serif
      text before any product, with the cover fan cropped below it, while
      desktop shows books beside the headline (which is why the desktop
      visitor clicked in seconds and bought). Fix: on ≤600px the hero is now
      product-first — book covers on top (visible at 102px), headline 4→3
      lines, sub-copy trimmed (2 sentences hidden on mobile only), full-width
      tap-friendly CTAs, covers repositioned inside the screen. CTA sits at
      604px, still above the 812px fold. Desktop verified unchanged
      (side-by-side hero, full copy).
      NEXT MEASURE: watch Clarity mobile sessions — target is any click at
      all from mobile; today's baseline is 0 clicks across 5 mobile visits.
- [ ] SEO (agreed 2026-08-28: START AT 3 SALES). Plan when triggered:
      (1) keyword-targeted articles on the same intents we buy ads for
      ("airbnb welcome book template", "house manual template", "what to put
      in a welcome book"), (2) each article ends in the builder CTA,
      (3) sitemap.xml + robots.txt + Search Console, (4) the 62 designs are
      a natural gallery page (long-tail image/design searches).
      Rationale: SEO compounds and is free, but takes 2-4 months to show —
      so it starts once the paid funnel is proven (3 sales), not before.
- [ ] Optional QA: $29 self-purchase + refund
- [x] EMAIL LIVE 2026-08-24: ImprovMX account (Mario's gmail; first attempt
      with hello@ was a dead-end — confirmation loop), domain Active,
      catch-all *@makewelcomebook.com → mario.otruba2003@gmail.com,
      MX (mx1/mx2.improvmx.com) + SPF added at GoDaddy by Claude, all ✓
- [ ] Google Ads campaign live (spec ready, gated on accountant answer)
- [ ] Etsy listing live (copy ready)

## Ads checkpoint 2026-08-28 (evening) — DEVICE SPLIT IS THE STORY

Window Aug 23-29 (sprint at €16/day, €2.00 max CPC since Aug 26):
  208 impressions · 11 clicks · CTR 5.29% · avg CPC €1.69 · spend €18.58
  1 conversion · cost/conversion €18.58 · net revenue €23.36 → profit ~€4.78

DEVICE BREAKDOWN (the decisive number):
  Desktop : 36 impr ·  4 clicks · CTR 11.11% · €7.83 · **1 sale** · CVR 25%
  Mobile  : 168 impr ·  6 clicks · CTR  3.57% · €8.80 ·  0 sales  · CVR 0%
  Tablet  :  4 impr ·  1 click  · CTR 25%    · €1.95 ·  0 sales

Read: mobile = 81% of impressions and ~47% of spend, zero revenue. Desktop =
17% of impressions and 100% of revenue, at 3x the CTR. Mario's instinct was
right. BUT every mobile click so far landed on the OLD mobile page; the
product-first mobile hero shipped 2026-08-28 ~1h before this checkpoint.

NOT budget-limited: spending ~€3/day of a €16/day budget → raising budget does
nothing; volume is capped by exact-match search volume, not money. Also means
cutting mobile would NOT push more budget to desktop (desktop is volume-capped).

DECISION: give the new mobile page a bounded test (through Sun 2026-08-31).
If mobile is still 0 conversions after ~10-15 more mobile clicks, apply a
-100% mobile bid adjustment. Note: device bid adjustment UI is not exposed for
this campaign in the current Google Ads interface (no Devices section under
campaign settings; Advanced bid adjustments only covers call interactions) —
if we need it, do it via Google Ads Editor or by rebuilding bidding.

OPEN ITEM (needs Mario, ~30 min, his ID): Google "advertiser verification"
is pending. It unlocks logos in ads (+3.7% opt score) and Google eventually
requires it. Claude must not submit identity documents — Mario does this.

### Bid raise 2026-08-28 (Mario spotted it): max CPC €2.00 → €2.80
Impression-share data proved the constraint was BID, not budget:
  Search impression share 34.83% · lost to RANK 65.17% · lost to BUDGET 0.00%
  Desktop (our only converting device) worst of all: IS 24.73%, lost to rank 75.27%
So we were invisible for ~3 of every 4 desktop searches by our best buyers,
while €16/day sat unspent. Budget stays €16 (still not binding).

BREAK-EVEN GUARDRAIL (net revenue per sale €23.36):
  blended CVR 9.09% → break-even CPC €2.12
  desktop CVR 25%   → break-even CPC €5.84   ← where the headroom is
  mobile CVR 0%     → every mobile click is currently pure cost
TRIPWIRE: if by Sun 2026-08-31 avg CPC > €2.20 AND no second sale → drop cap
back to €1.80 and cut mobile. If a desktop sale lands → hold or push higher.
NEXT VOLUME LEVER (after bid): all keywords are EXACT match. Adding phrase
match on the proven terms widens eligible searches without raising CPC.

### Geo correction 2026-08-28 — UK REMOVED, US prioritised
Mario asked why we were on UK at all. Honest answer: the original plan (this
file, "Channels") always said Geo = US, UK, CA, AU — my call at launch, to
widen a very small exact-match pool. It was never US-only. The data now says
that was the wrong call:

  UK  : 152 impr (73%) ·  8 clicks · €12.63 (68% of spend) · 0 sales
  USA :  40 impr (19%) ·  3 clicks · €5.95              · 1 sale (33% CVR)
  CA  :  13 impr · 0 clicks · €0     AU: 3 impr · 0 clicks · €0

WHY the UK ate the budget: cheaper auctions (UK avg CPC €1.58 vs US €1.98).
With a €2.00 cap we were priced out of most US auctions and easily won UK
ones, so Google spent where it could win — the wrong market.
DEEPER CAUSE — INTENT MISMATCH: the UK search terms were "guest book",
"guest book for holiday home / holiday let / home visitors", "visitor book".
In British English a "guest book" is the PAPER BOOK VISITORS SIGN, not a host
welcome manual. So most UK traffic wanted a different product entirely.

ACTIONS: United Kingdom REMOVED from targeting; United States bid adjustment
set to +50% (with the €2.80 cap → effective up to ~€4.20 in the US, still far
under the €5.84 US break-even). CA and AU kept (zero spend so far, same
North-American/English intent worth a cheap look).
EXPECT: fewer total impressions, higher share in the market that actually buys.
REVERSIBLE: re-add UK any time if we later target "welcome book"-only intent.

## ★★ SALE #2 — 2026-08-31, 12:09 ★★
joyce@mostlymail.us · $29.00 · Stripe Link · Succeeded · net ≈ €23.36
Running totals: 2 real sales (+ Mario's own test), net revenue ≈ €46.72.
Ad spend: €24.78 (to Aug 30) + €5.51 today = €30.29 → PROFIT ≈ €16.43.

WHY GOOGLE ADS SHOWS 0 CONVERSIONS FOR IT (checked, not guessed):
 1. Reporting window: Google's "last 30 days" ENDS YESTERDAY (Aug 30) — today's
    conversions cannot appear there at all. Today-only view: 45 impr, 2 clicks,
    €5.51, conversions still 0 (Google conversion reporting also lags hours).
 2. Only 2 ad clicks happened today. If Joyce arrived organically/direct there
    is no ad click to attribute — Clarity now shows a growing number of sessions
    with NO referrer (US, CA) plus google.com organic. Free traffic is starting.
 3. NOT a broken funnel: the Stripe Payment Link's confirmation page is
    https://makewelcomebook.com/app.html?paid=MWB-UNLOCK-2026 — verified today,
    so every payer is auto-redirected and unlocked. Joyce got her book.
ACTION: re-check tomorrow with today included; if it never registers, treat it
as an organic sale (good news) rather than a tracking fault.

SEO TRIGGER: 2 of 3 sales reached. One more and SEO work starts as agreed.

## Clarity full read + performance fix 2026-08-31

CLARITY (last 30 days, 109 sessions / 108 unique, own IP excluded):
  pages per session 1.09 · scroll depth 47% · active time 44s
  100% new users, 0% returning · dead clicks 8.26% (9 sessions)
  rage clicks 1 · quick backs 2 · JavaScript errors 0
  devices: Chrome desktop 44%, Chrome Mobile 39%, Mobile Safari 14% (~53% mobile)
  referrers: direct/internal 50, google.com 21, buy.stripe.com 1 (a payer returning)
  smart events: Download 5 sessions, Book 1 · top pages: / 56, app.html 49
  WEB VITALS: LCP 1.1s good · CLS 0.015 good · **INP 780ms POOR**

ROOT CAUSE FOUND: every keystroke ran save() + a FULL render() — rebuilding all
11 pages and regenerating the WiFi QR — with no debounce. Typing a property name
= ~23 full rebuilds. That is the poor INP and the 8.26% dead clicks.

FIX SHIPPED: renderSoon() debounce (130ms) on text/colour inputs + WiFi QR cached
by ssid+password. Selects/buttons still render instantly. Download flushes any
pending render first, so a PDF can never be stale.

MEASURED ON THE LIVE SITE (typing "Seaside Cottage Retreat", 23 keystrokes):
  renders triggered   23 → 1
  blocking time       ~200ms → 2ms  (0.1ms per keystroke)
  one render costs    9.1ms · QR rebuild 7.4ms → 0ms when cached
  correctness checks  preview updates after debounce ✓ · localStorage saves
                      immediately ✓ · click Download mid-typing flushes the
                      pending render before printing ✓
EXPECT: INP should fall from 780ms toward "good" (<200ms) as new sessions come in;
dead clicks should drop. Re-check Clarity vitals in a few days.

## Landing-page rebuild 2026-08-31 (Mario: "do all you can, best decisions")
Target: the biggest measured leak — 1.09 pages/session, i.e. visitors land and
never reach the builder. Decisions made and why:

1. DESIGN GALLERY (new section, 24 real covers at 260px, 184KB total, lazy after
   the first row). Rationale: Clarity shows engaged users explore themes for
   minutes (one session: 42 min / 139 clicks). The designs are the magnet, and
   they were invisible on the landing page. Copy: "62 designs — 38 premium art
   designs included free."
2. CTA AFTER EVERY SECTION: was 2 CTAs across a 9-screen page; now 7
   (hero, after How-it-works, after gallery, after comparison, pricing, footer,
   sticky). Intent can convert at any scroll depth.
3. STICKY MOBILE CTA — always visible on ≤820px. Deliberately CSS-only, no JS
   (see note below).
4. CORRECTED STALE COUNTS: "50 designs"→62, "26 premium"→38.
   Kept price honest at $29; NO fake "was $49" sale framing (false reference
   pricing is illegal under EU Omnibus/FTC and breaches Google's
   misrepresentation policy). Legit angle used instead: $29 once vs $99/year.

BUGS FOUND AND FIXED DURING VERIFICATION
 * Gallery cards rendered 105x368 instead of 105x149: the HTML height="368"
   attribute beat the CSS aspect-ratio (aspect-ratio is ignored when both
   width and height resolve). Fixed with height:auto. This was my own
   regression, caught before it reached traffic.
 * Sticky CTA first used a scroll listener, then IntersectionObserver — neither
   fired in the preview pane (the pane pauses rAF/IO callbacks, which also
   stops lazy images loading there). Rather than ship JS I could not verify,
   switched to a CSS-only always-on bar. Simpler and cannot fail.

VERIFIED: mobile 0 horizontal overflow, cards 0.707 ratio, 7 CTAs, sticky bar
visible on mobile / hidden on desktop, desktop hero still side-by-side,
gallery 9 columns on desktop, no console errors.

DECIDED AGAINST FOR NOW (with reasons)
 * Discount at the download step: both buyers paid full price without
   hesitation (Tarun in 81s). Only 5 people have ever reached that step, so a
   discount would cut margin on people who would have paid anyway. Revisit at
   ~20 download-step sessions.
 * Retention/email capture: Mario is right that this is a one-time purchase;
   0% returning visitors is expected, not a problem to solve.

## Google Search Console added 2026-08-31 (property: https://makewelcomebook.com/)
Reason: Mario asked whether sale #2 came from SEO. Clarity cannot tell paid from
organic (both show a google.com referrer) and Google Ads never logged a 2nd
conversion, so the question was unanswerable — Search Console is the only
instrument that reports organic queries/clicks. It was never set up (only
stckd.app existed in the account).

Verified by HTML meta tag added to index.html AND app.html:
  <meta name="google-site-verification" content="DGiT9xLwGc2ZGHIzvMIWtdzmIsBRBSfOWMrPVwZc_Ns">
DO NOT REMOVE these tags or verification is lost.

DELIBERATE CHOICE: Google offered one-click verification via a DOMAIN property,
but that flow grants Google access to Mario's GoDaddy DNS account. I did not
authorise that on his behalf — used the self-hosted meta tag instead, which I
control end to end. Trade-off: URL-prefix property does not cover
www.makewelcomebook.com (our canonical is non-www, so this is fine).

STATUS: "Data is processing, try again in about a day." So the SEO-vs-paid
question for sale #2 cannot be answered yet — check the Performance report
tomorrow. Known so far: the homepage IS indexed (confirmed via a site: search),
but the site is 9 days old with no backlinks, so ranking for competitive terms
like "airbnb welcome book template" is unlikely this soon.
NEXT (once data appears): read organic queries, then submit a sitemap when the
SEO phase starts at 3 sales.

## SEO groundwork done 2026-08-31 (technical only — content phase still gated at 3 sales)
 * robots.txt — allows all crawlers, points to the sitemap
 * sitemap.xml — 5 URLs (home, builder, terms, privacy, refunds), valid XML
 * canonical tags on index.html and app.html (prevents duplicate-URL dilution
   from ?sample=1 / ?paid= / ?v= query strings we use)
 * sitemap SUBMITTED to Search Console → status "Úspech" (Success),
   5 pages discovered, 0 errors
This is indexing hygiene, not content marketing: it helps Google find and
correctly attribute the pages we already have. The agreed SEO content work
(articles, gallery landing page) still starts at sale #3.

## CORRECTION 2026-08-31 (evening): sale #2 was PAID, not SEO — and it was a TABLET
Mario spotted the conversion registering; confirmed by setting the Ads date
range to today only (Google's default views end yesterday, which is why it
looked missing earlier).

TODAY (Aug 31): 68 impressions · 3 clicks · €8.03 · **1 conversion** · CVR 33%
  Desktop : 23 impr · 1 click · €2.73 · 0 conv
  Mobile  : 43 impr · 1 click · €2.52 · 0 conv
  Tablet  :  2 impr · 1 click · €2.78 · **1 conv (100%)**

So my earlier speculation that sale #2 might be organic was WRONG — it came
from a paid tablet click. It also matches the Clarity session I had already
watched (user 2y0yli, GoogleApp browser on tablet): arrived from Google,
clicked the "See a finished example" sitelink, browsed themes at 03:40, came
back at 13:25, built for 42 min / 139 clicks, downloaded the PDF preview twice,
clicked out to Stripe at 42:26. That IS the buyer.

RUNNING TOTALS (both sales ad-attributed):
  ad spend €32.81 · net revenue €46.72 · PROFIT €13.91 · ROAS 1.42x
  CPA €16.41 · 16 clicks · CVR 12.5%

IMPLICATIONS
 * The campaign is genuinely profitable, not accidentally so. Both sales paid.
 * TABLET deserves attention: 2 tablet clicks so far, 1 sale. I had written
   tablet off as negligible (4 impressions) — that was premature. The
   "dead clicks" Clarity flagged were also on this tablet/GoogleApp browser,
   which the render-debounce fix should have improved.
 * The "See a finished example" sitelink earned its place — it brought this buyer.
 * Search Console still worth having, but the SEO question is now answered for
   sale #2: it was paid. Organic remains unproven.

## Account health check 2026-08-31 (Mario spotted "Zameranie 1 kampane je nepotvrdené")
Checked everything that can actually stop ads. RESULT: no real errors.
 * Campaign status: Vhodné (Eligible), Active, serving — 3 clicks today
 * Ads: both RSAs Eligible, strength Priemerná (Average)
 * Keywords: all Eligible — zero disapprovals, zero low-search-volume flags
 * Sitelinks/callouts/snippets: approved earlier, still serving
 * Billing: balance €23.06 owed, next automatic charge 1 Sept — normal
   post-pay behaviour, card on file, no payment failure

WHAT THE MESSAGE ACTUALLY IS: "Targeting of 1 campaign is unconfirmed" sits on
the OPTIMIZATION SCORE (86.1%), not on the campaign. It means Google has not
re-confirmed the targeting since it changed — expected, because today I removed
the UK and set a US +50% bid adjustment. It does not block or limit delivery.
Optimization score is Google's advice metric, not a health metric; chasing it
would push us into things we deliberately rejected (AI Max, broad match,
dynamic images from the landing page).

STILL OUTSTANDING (needs Mario, cannot be delegated): advertiser verification.
No deadline shown in the account today, so it is insurance, not an emergency.

## FREE-TRAFFIC RESEARCH 2026-08-31 (Mario asked; summary of findings)
Ranked by expected value for THIS product (visual, $29 one-time, proven Etsy demand):
 1. ETSY — demand already proven (competitor: 8k reviews). Fees on $29 ≈
    $0.20 listing + 6.5% + 3%+$0.25 processing ≈ $3.30 (~11%); no ad cost.
    CAVEAT: Etsy digital listings deliver FILES; we sell an unlock. Deliverable
    = PDF guide containing personal unlock link (common practice, slight grey
    zone). Listing copy exists (ETSY-LISTING.md). Needs Mario: Etsy account.
 2. PINTEREST — the niche has its own trend page; product is 62 pinnable
    designs. Industry consensus: first sales in 60-90 days of consistent
    pinning; pins are evergreen (drive traffic for years). I can generate pin
    images from art/ + captions. Needs Mario: Pinterest business account.
 3. FREE TOOL PAGE — "Free Airbnb WiFi QR Sign Generator" standalone page.
    We already have client-side QR; the page ranks for "wifi sign airbnb free"
    style searches, gives value free, upsells the $29 book. Classic free-tool
    SEO magnet + backlink bait. I can build it solo.
 4. SEO ARTICLES — gated at 3 sales per earlier agreement (2/3 reached).
    Targets: "what to put in an airbnb welcome book", "house manual template",
    "airbnb welcome book template". 2-4 months to traffic. Groundwork done.
 5. REDDIT + FB HOST GROUPS — fast but manual and personal (accounts + genuine
    participation = Mario). High ban risk for drive-by promo. Opportunistic.
 6. PRODUCT HUNT / directories — one-time spike + backlinks; do after the
    free tool exists so there is something "launchable".
RECOMMENDED ORDER: Etsy now → Pinterest account now (compounding clock starts)
→ free WiFi-sign tool page (me, this week) → SEO articles at sale #3 →
PH launch after tool page. Reddit/FB whenever Mario feels like being social.

## Etsy + Pinterest launch kit BUILT 2026-09-01 (all in marketing/, gitignored — repo is public)
 * App change (deployed): second unlock code MWB-ETSY-2026 accepted; fires NO
   Google Ads conversion (marketplace sales must not pollute ad optimisation).
   Stripe keeps MWB-UNLOCK-2026 + conversion event.
 * marketing/etsy/Your-Welcome-Book-Access.pdf — branded delivery PDF with the
   Etsy unlock link + 4-step instructions (this is what Etsy auto-delivers)
 * marketing/etsy/1-main..6-onepage-sign.jpg — 6 listing images (cover fan,
   light grid, dark grid, what-you-get collage from the REAL sample-book PDF,
   sample cover, all-in-one sign)
 * marketing/etsy/sample-book.pdf — full 13-page watermark-free sample
 * marketing/pinterest/pin-01..38.jpg — 38 pins (1000x1500, 2:3) + pins.csv
   with per-design titles/descriptions/links
 * ETSY-LISTING.md updated (62 designs, file paths, $24.99 Etsy price)
WAITING ON MARIO: create Etsy shop + Pinterest business account; then I fill
both via his browser (listing upload, pin scheduling ~3-5 pins/day, not all 38
at once — Pinterest treats bulk-dumping as spam).

## Daily check 2026-09-01 (morning) — all healthy, no sale #3 yet
ADS last 7 days (Aug 25-31): 337 impr · 16 clicks · €34.29 · avg CPC €2.14.
Today so far: 4 impr, 0 clicks (EU morning, normal — US asleep).
Post-UK-cut device spend mix improved: desktop 50.3% of cost (was ~30%),
mobile 35.9%, tablet 13.8%. August month closed at €35.54 total ad cost.
BILLING VERIFIED: balance €25.54, Visa ••9123 on file, last €10 threshold
payment succeeded Aug 27, next auto-charge today (1.9. or at €50) — no
failures, nothing can silently stop ads. Red notification badge was only the
"add images to ads" recommendation nudge, not an account issue.
STRIPE: still 3 payments (Joyce, Tarun, Mario's test) · 0 refunds · 0 disputes.
CLARITY last 3 days (27 sessions): pages/session 1.09 → 1.48 and active time
44s → 3.4min — landing rebuild is measurably working; app.html is now the top
page (18 vs 13 views), so visitors DO reach the builder now.
JS ERRORS INVESTIGATED (11 errors, 11% of sessions — new since Aug 31):
filtered the error sessions — ALL THREE are Joyce (the buyer) revisiting her
unlocked book (entry app.html?paid=MWB-UNLOCK…) on her tablet in GoogleApp +
MobileSafari. Error text is the generic cross-origin "Script error." which
CANNOT come from our inline same-origin code — it's gtag/clarity inside her
tablet WebView. Reproduced the builder on the live site (type → debounced
render, page flips, unlock dialog): works, ZERO console errors. Not a
regression from the debounce fix; her sessions show normal use (31 more min
with her book). MONITOR: if "script error" starts appearing on NON-paid
sessions or other devices, investigate again.
INP: Clarity shows 1.4s "poor" but from ONE pageview (Joyce's tablet) — too
small to judge the Aug 31 debounce fix yet; re-check ~Sep 3-4.
SEARCH CONSOLE: still "data processing" (updated 7.5h ago) — organic
performance unreadable until ~Sep 2.
No actions needed today. Still waiting on Mario: (1) Etsy shop + Pinterest
account, (2) Google advertiser verification.

EVENING RE-CHECK 2026-09-01: ads today 21 impr · 2 clicks (both mobile) ·
€5.58 · avg CPC €2.79 (right at the €2.80 cap) · 0 conversions. Stripe still
3 payments — no sale #3. Clarity today: 9 sessions / 6 users, 60% scroll,
0 JS errors (confirms the Aug 31 errors were a one-off from Joyce's tablet),
app.html again top page (7 vs 2). Site: all 7 URLs 200 OK in ~0.2s, cert
valid to Nov 20, landing + builder render clean, zero console errors.
WATCH: avg CPC touching the cap with mobile-only clicks — if this repeats
2-3 days with no sale, revisit the mobile question (tripwire from Aug 28).

## ★ PHRASE MATCH ADDED 2026-09-02 (Mario: "we need to get clicks")
Sept 1 final: 55 impr · 4 clicks · €11.07 · 0 conv (best volume day post-UK,
but Mario saw zeros — Google default ranges exclude the current/previous day).
Volume is the bottleneck (39 exact-match keywords = tiny eligible pool), so
pulled the lever planned on Aug 28: added 11 PHRASE-match keywords on proven
buyer terms to Reklamná skupina č. 1:
  "welcome book template" · "airbnb welcome book" · "vacation rental welcome
  book" · "airbnb house manual" · "house manual template" · "guest information
  book" · "airbnb welcome guide" · "rental welcome book" · "welcome book for
  vacation rental" · "airbnb guest guide" · "short term rental welcome book"
Deliberately NOT phrased: [guest welcome book] (170 impr at only 1.76% CTR —
widening a weak term wastes money; UK "guest book" intent lesson).
Status on save: Nespracované/Prebieha kontrola (normal review, serves in
hours). Budget stays €16/day, CPC cap €2.80, 54 negatives still guard.
EXPECT: impressions should rise 2-5x within ~2-3 days. NEXT: mine the
search-terms report ~Sep 4-5 — phrase match WILL let in some junk; add
negatives weekly. ROLLBACK: pause the 11 phrase keywords if CPA blows past
~€20 with no sale.

## ★★ ETSY SHOP LIVE 2026-09-02 ★★ (Mario: "only Etsy, no Pinterest")
Shop: https://www.etsy.com/shop/MakeWelcomeBook (name MakeWelcomeBook,
English / Slovakia / USD, location Slovakia, tagline "Vacation rental welcome
books, finished in 10 minutes", W-monogram icon + banner from our art).
Listing: https://www.etsy.com/listing/4566989528/welcome-book-maker-for-airbnb-vacation
  $24.99 · qty 999 · Digital · category Design Templates · auto-renew ·
  featured on shop home · 13 tags · AI-generator disclosure ticked (the art
  backgrounds are Higgsfield output — Etsy requires this and it is honest).
  Digital files delivered: Your-Welcome-Book-Access.pdf (Etsy unlock link
  MWB-ETSY-2026 + steps) AND sample-book.pdf (13-page real sample) — the
  second file makes the download a real deliverable, not just a link.
Account setup was Mario's part (bank IBAN/ID/card/2FA, $19 one-time fee).
Registered with hello@makewelcomebook.com — Etsy verification codes land in
Gmail SPAM via ImprovMX; read them from ImprovMX → domain → Logs if needed.
IMAGES REBUILT (marketing/etsy/, old versions kept as old-*.jpg): the
original 1-main/2-light/3-dark were raw art backgrounds with NO text — an
Etsy shopper couldn't tell what the product was. New set via Pillow script
(scratchpad build_etsy_assets.py; fonts Fraunces+Inter, brand tokens):
  1-main.jpg 2000x1500 — headline + 3-cover fan (sample cover + 2 synthesized
  titled covers) · 2/3 grids — 8 synthesized covers each with real-looking
  property names · shop-icon.png 1000² · shop-banner.jpg 2400x600.
Shop policies: Etsy locks digital items to "no returns" preset — our 14-day
money-back still honored manually via refund if a buyer messages.
NOT done: website link in About (Etsy's link widget rejected input twice;
low value, Etsy discourages off-site links). Pinterest kit shelved by Mario.
Price note: EU viewers see $30.74 (Etsy adds Slovak VAT on display); US
buyers see $24.99. Estimated net per sale ≈ $21.82 (Etsy's own estimate).
★ HIGGSFIELD PRODUCT PHOTOS 2026-09-02 (Mario: "it looks terrible, really use
Higgsfield"). Drove higgsfield.ai in his Chrome (Google SSO, his gmail),
model Nano Banana Pro 4K, 4:3, with OUR real cover / sign uploaded as
reference images so the mockups show the actual product:
  1-main.jpg        booklet on marble counter, eucalyptus + coffee (cover text
                    rendered perfectly by the model)
  2-book-and-sign   booklet + framed sign on wood table, dried flowers
  3-framed-sign     oak-framed sign on entryway console, olive tree, keys bowl
  4-bedroom         booklet on nightstand, linen bed, lamp, succulent
  5-8 = cover grids (light/dark), what-you-get, typographic headline (old main)
LESSON: the model reproduces LARGE cover text faithfully but garbles small
body text on the sign → fixed by compositing the real src-sign.jpg onto the
frame with a perspective warp + polynomial-fit lighting (scratchpad
composite_sign2.py; frame corners measured from ruler crops). The sign file
has a 13px white page margin — crop to art bbox before warping.
GOTCHAS: 1st generation was falsely flagged NSFW (credits refunded) — just
re-run; the landing-page upload attached Higgsfield's pink mascot as the
reference instead of our cover — always verify the thumbnail in the prompt
bar before generating (each run costs 4 credits, ~60-90 s at 4K).
Shop banner rebuilt from the marble photo (wordmark panel on the right).
Originals: marketing/etsy/hf-4k/ (4800x3584) · v1 images in marketing/etsy/v1/.
NEXT: watch Etsy Stats daily (views/favorites); first review matters most —
after sale #1, message the buyer politely asking for a review. Consider a
2nd listing variant (e.g. "WiFi QR sign + welcome book bundle") once the
first shows views, since Etsy rewards multi-listing shops.

## ★ 2026-09-02 (late) — ETSY SALE LIVE + ADS CLEANUP + AUDIT REPORTS
ETSY SALE created: 30 % off, Everywhere, whole shop (auto-includes any future
listing), 2 Sep – 1 Oct 2026, name LAUNCH30. Public listing verified live:
US buyers see $20.30 (from $29); Mario's Slovak view shows $24.97 struck from
$35.67 — same thing with Slovak VAT added on display. Reference price is our
real site price ($29), so no fake-sale problem.
GOOGLE ADS (campaign 24166614210 only — the account also holds TenderEulogy):
 * Mobile device bid adjustment set to −50 % (Znížiť 50). The Zvýšiť/Znížiť
   control is a Material button-menu, not a <select>: click the button, then
   click the second item in the tiny popup list; form_input will not work.
   Verified in the Zariadenia table: Mobily = "-50 %".
   Rationale: mobile all-time 315 impr / 11 clicks / €21.66 / 0 conversions.
 * Campaign negatives added, phrase match: "guest book", "guestbook"
   (54 → 56 negatives). Kills ~44 % of all-time spend that went to physical
   guest-book searches. [guest information book] and [guest welcome book]
   deliberately survive — no contiguous phrase match.
 * Paused: [vacation rental guest book] (low-QS flag, 5 clicks, €9.67, 0 conv)
   and [vacation rental guest book template]. Verified "Pozastavené".
 * Unchanged on purpose: Maximize Clicks, €2.80 CPC cap, US +50 %, CA/AU on,
   €16/day budget, AI Max / broad / search partners OFF.
REPORTS WRITTEN (both in repo root):
 * ADS-AUDIT-2026-09-02.md — full audit. Key conclusions: campaign was at
   −€7.94 (CPA €27.33 vs €23.36 net) purely because of the guest-book waste;
   post-cleanup CPA should land near €15 (≈ +€8/sale). Budget is NOT the
   constraint (IS lost to budget 2.6 %, to rank 62.4 %). Relevant US demand is
   ~1,200–1,400 searches/month and the head terms are down 46–64 % YoY, so
   Google Search caps out at ~5–8 sales/month (≈ €40–70 profit). It is a floor,
   not a ladder. Kill criterion: next €40 post-cleanup with 0 sales → pause.
 * REALITY-CHECK-1000-EUR.md — honest answer to "can this make €1,000
   profit/month". Needs ~50 sales/month (1.7/day) at a blended €20 net; we are
   at ~4 % of that. Possible in 3–6 months only as a multi-channel build with
   Etsy as the engine (reviews compound), plus a $49 multi-property tier to
   lift AOV, plus organic/WiFi-tool traffic. Estimated ~1-in-4 odds within six
   months; base case €300–600/month. ⚠️ €1,000/month = €13–15k/yr revenue =
   6× the €2,200 no-živnosť ceiling, crossed in ~10 weeks at that rate —
   accountant must be consulted BEFORE scaling. Current real revenue ≈ €49
   (2 genuine Stripe sales; the 3rd payment was Mario's own test).
NOW PASSIVE for a few days per Mario. Daily checks only: Google Ads with date
range "Včera" (Google's default ranges hide today/yesterday), Stripe payments,
Etsy Stats (views/favorites), Clarity. Next active task: mine the search-terms
report ~4–5 Sep for junk let in by the 11 phrase keywords.

## DECISION 2026-09-02 (evening, Mario) — HOLD ONE DAY, THEN OPTIMIZE OR CUT
Mario: "we wait till tomorrow, I will tell you check ads, then by data we have
we will optimize everything; if no, we cut budget for 5 days and see more."
NO CHANGES TONIGHT. Budget stays €16/day, phrase keywords stay live, mobile
−50 % stays.
State at the moment of this decision (2 Sep, day not finished):
  All time 23 Aug – 2 Sep: 454 impr · 29 clicks · €68.11 · 2 conv · CPA €34.06
  2 Sep so far: 53 impr · 8 clicks · CTR 15.09 % · €21.75 · avg CPC €2.72 ·
    0 conv · impression share lost to BUDGET 21.88 % (first time ever non-zero)
  Mobile took 6 of 8 clicks and €16.21 of €21.75 today (−50 % applied midday).
  Clarity 3 d: 37 sessions, 5.7 min active, 0 rage clicks, JS errors = the same
    Aug-31 buyer tablet sessions (not new). Dead clicks 18.92 % — look later.
  Etsy all-time: 0 visits / 0 orders (shop <2 days old, stats lag 4 h).
  Stripe: still 3 payments, 0 refunds, 0 disputes — no sale #3.
  Budget left of the €250: ≈ €160.
TIMING CAVEAT for tomorrow: on 3 Sep, "Včera" = 2 Sep, which is a COMPLETE day
but only partly clean (mobile −50 % landed midday). The first FULLY clean day is
3 Sep, readable on 4 Sep. Say this out loud before making the call.
AGREED DECISION RULE:
  * ≥1 sale on 2–3 Sep → keep €16/day and optimize (mine search terms, add
    negatives, consider keyword-level bids on the two converters).
  * 0 sales and cumulative spend over 2–3 Sep ≳ €35 → CUT the daily budget for
    5 days (proposal: €16 → €8) and re-read on ~9 Sep.
Mario pings when he wants the check; do not run it unprompted.

## ★ 2026-09-03 (morning) — NO SALES → BUDGET CUT €16 → €8/day
Mario: "no sales". Verified before acting:
 * Stripe: still 3 payments (Mario test 8/24, Tarun 8/28, Joyce 8/31), 0 refunds,
   0 disputes. No sale #3.
 * Etsy all-time (Sep 1 – Sep 3): 0 visits, 0 orders, $0.00, 0 favorites,
   0 follows, 0 reviews. Shop is 2 days old; stats lag ~5 h.
 * Ads 2 Sep FULL day: 53 impr · 8 clicks · CTR 15,09 % · €21,75 · avg CPC
   €2,72 · 0 conv · impression share 18,22 % · lost to RANK 34,20 % ·
   LOST TO BUDGET 47,58 %.
 * Ads 3 Sep by 10:00 CEST: 26 impr · 0 clicks · €0,00 (US asleep — normal).
 * Ads all-time 23 Aug – 2 Sep: 454 impr · 29 clicks · €68,11 · 2 conv ·
   CPA €34,06.
ACTION TAKEN (per the decision rule agreed 2 Sep): campaign daily budget
lowered €16,00 → €8,00. Verified in the campaign row and header ("8,00 €/deň").
Nothing else touched: Max Clicks, €2,80 CPC cap, US +50 %, mobile −50 %,
56 negatives, 11 phrase keywords, 2 paused keywords — all unchanged.
WHY €8: on 2 Sep the campaign spent €21,75 (136 % of a €16 budget — Google
allows up to 2× on a day) and still lost 47,6 % of impressions to budget. At
that burn the remaining ≈ €160 of the €250 lasts ~8 days. €8/day gives ~5 days
of data for ~€40 and keeps the campaign learning instead of pausing it.
TWO REAL FINDINGS FROM 2 SEP:
 1. The negatives WORK on relevance: CTR jumped 4,77 % → 15,09 %.
 2. My 2 Sep audit line "budget is not the constraint" is now WRONG for the
    post-cleanup campaign. Before: lost-to-budget 0–2,6 %. On 2 Sep: 47,58 %.
    Filtering the junk + the 11 phrase keywords made the eligible pool both
    smaller and much more relevant, so €16/day genuinely binds. Corrected here
    and in ADS-AUDIT-2026-09-02.md.
NEXT REVIEW ~8–9 Sep (5 days at €8). Decision rule for then:
 * ≥1 sale → keep €8/day, optimise (search terms, bids on the 2 converters).
 * 0 sales after ~€40 more spend → PAUSE the campaign and move everything to
   Etsy/organic. That is the kill criterion from ADS-AUDIT-2026-09-02.md.
⚠ NEW PRIORITY PROBLEM — ETSY 0 VISITS IN 2 DAYS. A listing that showed on
page 1 for "airbnb welcome book template" on 2 Sep should get *some* views.
Either the new-listing boost has already passed, or the listing is not being
surfaced. To check next session: Etsy Shop Manager → "Etsy search visibility",
and search Etsy in a logged-out/incognito window for the main terms to see
where (or whether) the listing ranks. This now matters more than the ads.

## Daily check 2026-09-03 21:10 CEST — stats table (overall / 24 h / 48 h)
ADS (campaign 24166614210 only):
  Overall 23 Aug – 3 Sep: 514 impr · 30 clicks · CTR 5,84 % · €71,10 ·
    avg CPC €2,37 · 2 conv · CPA €35,55
  2 Sep (full): 53 impr · 8 clicks · CTR 15,09 % · €21,75 · CPC €2,72 · 0 conv ·
    IS 18,22 % · lost rank 34,20 % · lost BUDGET 47,58 %
  3 Sep (to 21:10): 60 impr · 1 click · CTR 1,67 % · €2,99 · CPC €2,99 ·
    0 conv · IS 27,87 % · lost rank 72,13 % · lost budget 0,00 %
  Devices 2 Sep: desktop 10/2/€5,54 · mobile 41/6/€16,21 · tablet 2/0
  Devices 3 Sep: desktop 50/1/€2,99 · mobile 10/0/€0 · tablet 0/0
  → MOBILE −50 % IS WORKING: mobile share of impressions 77 % → 17 %.
  → €8 budget NOT binding today (spent €2,99 of €8, 0 % lost to budget).
    Yesterday's 47,58 % budget loss was a one-day spike, not a new baseline.
  → CTR swing 15,09 % → 1,67 % is on 53 and 60 impressions — both samples are
    far too small to conclude anything. Do not act on it.
CLARITY:
  Overall (last 30 d = lifetime): ~146 sessions (141 new + 5 returning) ·
    131 unique users · 1,19 pages/session · 49,57 % scroll · 2,0 min active
    (of 2,7 total) · rage 0,68 % (1) · dead clicks 9,59 % (14) ·
    quick backs 1,37 % (2)
  2 Sep: 12 sessions (7 bots excluded) · 11 users · 1,33 pages · 51,50 % scroll ·
    1,9 min active · dead clicks 8,33 % (1) · rage 0 · quick backs 0
  3 Sep: 2 sessions (1 bot excluded) · 2 users · 1,50 pages · 54,33 % scroll ·
    36 s active · all insight metrics 0
ETSY: all-time / 2 Sep / 3 Sep all ZERO — 0 visits, 0 orders, $0,00,
  0 favorites, 0 follows, 0 reviews. Stats 4 h stale. Day 3 of the shop.
STRIPE: 3 payments (2 real + Mario's test), all $29, 0 refunds, 0 disputes.
  Nothing new in 48 h.
MONEY: €71,10 ad spend vs ~€46,72 net from 2 real sales → ≈ −€24.
NO ACTION TAKEN. Budget stays €8/day. Next review ~8–9 Sep per the agreed rule.
STILL THE #1 PROBLEM: Etsy 0 visits in 3 days. Investigate search visibility
next — this outranks anything left to tune in Google Ads.

## ★ CLARITY DEEP-DIVE 2026-09-03 — WHAT VISITORS ACTUALLY DO
Read all 55 recordings for the last 7 days (Aug 28 – Sep 3) plus the desktop
landing-page click heatmap. Findings:

SESSION MIX. Of the 55 sessions, roughly a third are the TWO EXISTING BUYERS
re-opening their book via app.html?paid=MWB-UNLOCK-2026 — long, healthy
sessions (1 h 22 m / 42 m / 31 m / 24 m, 76 / 139 / 36 clicks). They appear as
~9 different Clarity user IDs because Clarity issues one ID per browser+device
and the delivery is an emailed link opened on phone, tablet, Safari, GoogleApp
etc. CHECKED FOR A LEAK: `site:makewelcomebook.com` on Google returns ONLY the
homepage — the unlock URL is NOT indexed. No evidence the code is leaking.
Product usage by buyers is genuinely deep. That is the good news.

REAL PROSPECTS (~34 non-buyer sessions in 7 days):
 * ~20 bounced in under 30 s with ZERO clicks (many at 1–5 s).
 * ~6 engaged properly (>1 min with clicks); almost ALL of them Chrome on PC.
 * ~5 reached app.html or the sample.
 * The mobile sessions bounce at close to 100 %: MobileSafari / ChromeMobile
   entries lasting 0:01–0:29 with 0 clicks, over and over.
 * The one converter in the window (Aug 28, user hdsjwy, Chrome PC) spent
   8:30, 57 clicks, 5 pages → that is what a buyer session looks like.
→ This is independent confirmation that the mobile −50 % bid adjustment was
  correct. Desktop visitors engage; mobile visitors leave instantly.

LANDING-PAGE CLICK HEATMAP (desktop, 7 days): 22 page views → only 5 CLICKS in
total, on just two elements:
   A.btn.btn-ghost "See a finished example" — 3 clicks (60 %)
   A.btn.btn-primary "Build my welcome book" — 2 clicks (40 %)
→ THE SECONDARY BUTTON OUT-PULLS THE PRIMARY CTA. People want proof before
  they will start. Worth testing: lead with the example/sample, or put a real
  finished book above the fold instead of the three stylised covers.

DEAD CLICKS (14,55 %, 8 sessions) are NOT a landing-page problem — every one
is inside app.html / the sample viewer, and 6 of the 8 are the two buyers.
People click things in the builder/sample that do not respond. Low priority
but a real polish item; likely the sample pages (someone clicked 139 times in
42 minutes on app.html?sample=1).

FALSE ALARM CHECKED: the Clarity heatmap screenshot renders the hero as
"finished in □□ minutes" and "□□ designs". Loaded the LIVE site — it correctly
shows "finished in 10 minutes" and "62 designs · 38 premium art designs FREE".
Clarity is masking numerals for privacy. The page is fine. Mobile layout also
verified at 375×812: headline, both CTAs and the sticky bottom bar are all
above the fold. The mobile bounces are NOT a broken layout.

ONE THING TO FIX IN ADS: a paid click (gclid present) landed directly on
app.html?sample=1 and bounced in 5 s. A sitelink is dropping people straight
into the sample viewer instead of the landing page. Check the 4 sitelinks next
time the ads account is open.
