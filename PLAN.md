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
