# Mario's steps — everything Claude cannot do for you

Do them in order. Each one is short. Everything else is already done or waits
only on these.

## Step 0 — TODAY, 2 minutes: the accountant message

Send your accountant this (Slovak is fine):

> "Predávam digitálne produkty (PDF návody) cez vlastné weby do zahraničia,
> platby cez Stripe. Potrebujem živnosť pred spustením reklamy? A mám sa
> registrovať na DPH/OSS pre predaj digitálnych produktov do EÚ?"

We do NOT turn on paid ads until this is answered. (It covers Reset Histamine
AND the new site at once.)

## Step 1 — 1 minute: let Claude publish the site

Claude tried to publish the website to your GitHub account (free hosting,
nothing to pay) and was blocked by a permission check — publishing needs your
OK. Next time you're in the chat, just say:

> "yes, publish the site to GitHub"

and Claude does the rest, including giving you a working link.

## Step 2 — 5 minutes: buy the domain (~€12/year)

When Claude says the site is live on the temporary link:

1. Go to **godaddy.com** (you already have an account from resethistamine)
2. Search: **makewelcomebook.com**
3. Buy the plain domain. Say NO to everything they try to add (privacy is
   already included, you don't need email packages, hosting, or "premium DNS")
4. Tell Claude "domain bought" — Claude gives you the 2 DNS records to paste
   (same screen you used for resethistamine)

## Step 3 — 5 minutes: Stripe payment link

1. Go to **dashboard.stripe.com** → log in (same account as resethistamine)
2. Click **Product catalog** → **+ Add product**
   - Name: `MakeWelcomeBook — Welcome Book Unlock`
   - Price: **$29.00**, One-time
3. Click **Payment links** → **+ New** → choose that product
4. After creating it, open the link's settings → **After payment** →
   **Redirect customers to your website** and paste EXACTLY:
   `https://makewelcomebook.com/app.html?paid=MWB-UNLOCK-2026`
5. Copy the payment link (starts with `https://buy.stripe.com/...`) and paste
   it to Claude in the chat. Claude wires it into the site.

## Step 4 — 15 minutes: new Google Ads account

Only after Step 0 is answered and the site is live on the real domain:

1. Go to **ads.google.com** → **Start now** → sign in with your Google account
2. IMPORTANT: it will push a "Smart campaign" wizard. Look for the small link
   **"Switch to Expert Mode"** (bottom of the screen) and click it
3. Then click **"Create an account without a campaign"** (small link again)
4. Confirm country/timezone/currency: Slovakia / Bratislava / EUR
5. Go to **Billing** → add your card
6. If Google asks for "advertiser identity verification" — do it with your real
   name and documents; it's normal for new accounts
7. Tell Claude "ads account ready" — Claude builds the whole campaign from
   ADS-CAMPAIGN.md and shows you the projected spend BEFORE anything runs.
   Nothing spends money until you personally see it and say "go".

## Step 5 — later, optional: Etsy shop (free second channel)

When the site is making its first sales, open an Etsy shop (etsy.com/sell,
shop name "MakeWelcomeBook") — listing text is ready in ETSY-LISTING.md.
