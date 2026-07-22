# First-party ordering & checkout — build/cost plan

**Prepared:** 22 Jul 2026 · for shamiatrestaurant.com
**Status:** decision doc (not yet built). Static fixes shipped separately today.

## The problem (confirmed from the audit)

Today all ordering funnels either to **WhatsApp** (call / message / "Send order on WhatsApp" builder) or to **six delivery aggregators** (Talabat, noon, Deliveroo, Careem, Keeta, Smiles).

- **Delivery-app dependency** — aggregators charge ~**25–35% commission** per order and *own the customer*. You don't get the diner's name, number, or repeat-order data; they do.
- **No first-party data** — WhatsApp gives you the phone number (good) but no structured order history, no re-marketing list, no card-on-file, no automatic totals/receipts.
- **Manual load** — every WhatsApp order is keyed in by hand and the total is confirmed back and forth.

WhatsApp is *not* the villain here — it's first-party (goes to your phone) and free. The leak is the **aggregators**. The upgrade is a **direct online checkout** that captures the customer and the payment, so aggregators become the fallback, not the default.

> Today's shipped static fix already pushes "Order direct — no extra app fees" above the apps and demotes the aggregator row. This doc is the next step: a real checkout.

## What a real checkout needs (why it's not a static-file edit)

GitHub Pages serves static files only — no server, no database, no secret keys. A checkout needs four things Pages can't do:

1. **Menu + cart** — *(can* be static; the site already has an order builder)*
2. **Payment capture** — card/Apple Pay/Google Pay → needs a **payment gateway** + a server-side secret key
3. **Order storage + kitchen notification** — a database + a way to alert the kitchen (WhatsApp/print/dashboard)
4. **Order status** — confirmation, prep, out-for-delivery

## Three ways to build it (cheapest → most control)

### Option A — Hosted ordering platform (fastest, lowest effort) ✅ recommended first
Plug in a UAE-friendly restaurant-ordering SaaS and embed/link it. It handles menu, checkout, payments, kitchen notifications and a customer list for you.

- **Examples to price:** Chatfood, Ordable, iKentoo/Lightspeed, UrbanPiper, or a Careem/Talabat "direct" white-label storefront.
- **Cost:** typically **AED 0–500/month** + ~2–2.9% payment-processing (vs 25–35% aggregator commission).
- **Effort:** ~1–2 days to configure the menu + embed a "Order online" button. No code hosting change.
- **Owns:** customer list, order history, promos — all yours.
- **Trade-off:** monthly fee; less bespoke look than a custom build.

### Option B — Static site + serverless checkout (custom, low monthly)
Keep the current site; add a checkout backed by a payment link / serverless function.

- **Simplest sub-variant:** **Stripe Payment Links / Telr / Ziina / Tap Payments** — generate a pay link per order, or a hosted checkout. Order details still arrive via WhatsApp, but **payment is captured up front** and you get an email/dashboard record.
- **Fuller sub-variant:** a serverless function (Cloudflare Workers / Vercel Functions — free tiers) writes the order to a DB (Airtable/Supabase free tier) and fires a WhatsApp/Telegram notification to the kitchen.
- **Cost:** **~AED 0–75/month** + gateway fees (Tap/Telr ~2.5–3% + small per-txn; Ziina low-fee UAE).
- **Effort:** ~3–6 days. Requires one small backend (serverless) — the site itself can stay on Pages.
- **Trade-off:** you maintain a little code; gateway onboarding needs a UAE trade licence + bank account.

### Option C — Full custom ordering app (most control, most cost)
Move to a Next.js/app host (Vercel/Netlify) with menu DB, cart, accounts, card-on-file, order tracking, kitchen dashboard.

- **Cost:** hosting ~AED 0–150/month + gateway fees + build time.
- **Effort:** ~2–4 weeks.
- **Only worth it** once direct-order volume is high enough to justify owning the whole stack.

## UAE payment gateways (for Option B/C)

| Gateway | Notes | Rough fee |
|---|---|---|
| **Tap Payments** | UAE/GCC-native, cards + Apple/Google Pay, good docs | ~2.5–3% + per-txn |
| **Telr** | UAE, widely used by restaurants | ~2.9% + per-txn |
| **Ziina** | UAE fintech, simple pay links, low fee | low % |
| **Stripe** | Now live in UAE, best DX, Payment Links need no code | ~2.9% + AED 1 |
| **Network / N-Genius** | Emirates NBD, bank-grade | negotiated |

All require a **trade licence + UAE business bank account** in the restaurant's name.

## Recommendation

1. **Now:** keep the shipped static fix (direct-order default, apps demoted, dedicated /catering/ page). Zero cost, live today.
2. **Next (2 weeks):** trial **Option A** (a hosted ordering platform) — lowest effort, immediately recovers the ~30% aggregator commission on direct orders and starts building a first-party customer list. Add an "Order online" button next to the WhatsApp CTA.
3. **If volume grows / you want a bespoke checkout:** move to **Option B** with **Tap or Ziina** + a serverless order notifier, keeping the site on Pages.

## Decisions needed from the owner

- [ ] Is there a UAE trade licence + business bank account ready for a gateway? (gates Options B/C)
- [ ] Monthly-fee tolerance (Option A) vs one-time build + maintenance (Option B)?
- [ ] Do we want card capture *now*, or just an order record + WhatsApp payment for the first phase?
- [ ] Preferred gateway (Tap / Ziina / Telr / Stripe)?

*Nothing here changes the catering flow — catering stays WhatsApp/phone/email by design, as confirmed.*
