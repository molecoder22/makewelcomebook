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
- [ ] Optional QA: $29 self-purchase + refund
- [ ] Free email: Mario signs up improvmx.com (1 min) → Claude adds MX records
- [ ] Google Ads campaign live (spec ready, gated on accountant answer)
- [ ] Etsy listing live (copy ready)
