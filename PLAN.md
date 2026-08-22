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
- [ ] NEXT GATE: accountant živnosť answer → then new Google Ads account →
      build campaign from ADS-CAMPAIGN.md (paused) → Mario approves spend
- [ ] Optional QA: $29 self-purchase + refund
- [ ] Free email: Mario signs up improvmx.com (1 min) → Claude adds MX records
- [ ] Google Ads campaign live (spec ready, gated on accountant answer)
- [ ] Etsy listing live (copy ready)
