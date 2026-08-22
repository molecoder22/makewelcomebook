# Google Ads — Launch Campaign Spec (ready to build)

Everything below is decided; Claude will build it in the Ads interface once the
account exists. Budget rules from PLAN.md apply: €200 max for ads, kill at €120
spent with zero sales.

## Account & campaign settings

- New Google Ads account (Mario's decision — separate from histamine account)
- Skip Google's "Smart campaign" onboarding — switch to Expert mode
- Campaign type: Search only (Display OFF, Search Partners OFF)
- Campaign name: `WB-Search-Templates`
- Daily budget: €8/day (≈ 25 days of runway on €200)
- Bidding: Manual CPC, max CPC €1.00 (raise to max €1.50 only on keywords with
  impressions but no clicks after 3 days)
- Locations: US, UK, Canada, Australia — setting "Presence" (people IN them)
- Language: English · Networks: Google Search only

## Ad group 1: `welcome-book` (exact match keywords)

[airbnb welcome book template] · [airbnb welcome book] · [welcome book for
airbnb] · [vacation rental welcome book] · [airbnb guest book template] ·
[welcome book template]

## Ad group 2: `house-manual` (exact match keywords)

[airbnb house manual template] · [airbnb house manual] · [vacation rental house
manual] · [airbnb guest guide template]

## Negative keywords (campaign level)

free, pdf free, canva free, example, examples, ideas, what is, diy, job, jobs,
course, physical book, hardcover
(People searching "free" will never pay $29 — don't buy their clicks.)

## Responsive Search Ad (both ad groups)

Final URL: https://makewelcomebook.com

Headlines (no "Airbnb" in ad text — trademark policy):
1. Your Welcome Book, Done In 10 Min
2. Skip Canva — Answer 12 Questions
3. Welcome Book Generator For Hosts
4. $29 Once — No Subscription
5. WiFi QR Sign Included
6. Print-Ready Vacation Rental Book
7. See Your Whole Book Before Paying
8. 34 Designer Themes Included
9. Made For Short-Term Rental Hosts
10. Guests Stop Asking For The WiFi

Descriptions:
1. Answer a few questions about your place — get a beautiful print-ready welcome book. No design skills needed.
2. Try the full builder free. You only pay to download. $29 one-time, unlimited edits forever.
3. Welcome book, house rules sign, WiFi QR code and check-out card. Everything your rental needs.
4. Cheaper than one cleaning fee. Faster than one Canva evening. 14-day money-back guarantee.

## Conversion tracking

- "Purchase" conversion: gtag fires on post-payment unlock (Claude adds the
  snippet to app.html once the account provides the tag ID; value $29).
- Observation only: "StartedBuilder" — visited app.html.

## Launch checklist

- [ ] Ads account created + billing added (Mario)
- [ ] Keyword Planner check BEFORE enabling: core CPC estimates ≤ €1.50,
      otherwise stop and rethink
- [ ] gtag conversion snippet deployed
- [ ] Campaign built exactly as above, starts PAUSED
- [ ] Mario says "go" → enable
- [ ] Day 3 / 7 / 14 reviews: CTR, CPC, search-terms report → add negatives

## Kill / scale rules (from PLAN.md)

- €120 spent, zero sales → pause all, fix funnel, only then resume
- Keyword with 40+ clicks, no sale → pause it
- Keyword that produces a sale → more budget share, max CPC still ≤ €1.50
