---
name: shamiat-friday
description: >-
  Weekly Friday-morning "make noise" routine for Shamiat Restaurant
  (shamiatrestaurant.com), Duja Tower, Sheikh Zayed Road. Runs the local
  SEO / GEO / AEO + hotel lead-gen loop for the ~2km radius around Dubai
  World Trade Centre, Sheraton Grand and the SZR hotels: checks AI-search
  and local visibility, refreshes hotel-targeted on-site content, writes the
  week's hotel-guest social posts (EN + AR), drafts concierge outreach to a
  rotating set of nearby hotels, and logs KPIs. Use when the user says
  "run the Friday routine", "make noise", "weekly run", or "shamiat friday".
---

# Shamiat — Weekly Friday "Make Noise" Routine

**Goal:** keep the phones ringing. Every Friday, win the local + AI search
race for the hotels within ~2 km of Duja Tower (Dubai World Trade Centre,
Sheraton Grand, Fairmont, voco, Novotel/Ibis WTC, Four Points SZR, Towers
Rotana, Crowne Plaza, and the rest of the Sheikh Zayed Road cluster) and put a
booking/WhatsApp prompt in front of their guests and concierges.

**Business facts (source of truth — keep in sync with `llms.txt`):**
- Shamiat Restaurant (مطعم شاميات) — Syrian / Lebanese / Levantine, halal
- Duja Tower, Ground Floor, Sheikh Zayed Road, Trade Centre First, Dubai
- Coords 25.22885, 55.286282 · opposite Dubai World Trade Centre
- Open daily 12:00 PM – 5:00 AM · 4.5★ (~1,300 reviews)
- Phone / WhatsApp: +971 54 781 6266
- Delivery: Talabat, noon, Keeta, Smiles, Deliveroo, Careem

Run the seven steps in order. Keep it to one focused pass — this is a weekly
heartbeat, not a rebuild. End with the GM summary (Step 7).

---

## Step 1 — Visibility check (GEO + local pack)

Use `WebSearch` (and WebFetch where useful) to check whether Shamiat surfaces
for the money queries. Record YES/NO + rough position for each:

- "Syrian restaurant near World Trade Centre Dubai"
- "Arabic restaurant near Sheraton Grand Dubai"
- "restaurant near voco / Fairmont / Novotel Sheikh Zayed Road"
- "late night food near Dubai World Trade Centre"
- "Levantine / mansaf / manakish near Sheikh Zayed Road"
- "best Syrian restaurant Sheikh Zayed Road"

Also ask an AI-answer style question ("Where can hotel guests near DWTC eat
authentic Syrian food late at night?") and note whether Shamiat is cited.
Flag any query where Shamiat is missing — those are this week's targets.

## Step 2 — On-site hygiene

Confirm these are still true on `index.html` (fix if drift is found):
- `Restaurant` + `FAQPage` + `BreadcrumbList` JSON-LD present and valid
  (validate by parsing each `<script type="application/ld+json">` block).
- `#hotels` section present and the named-hotel chips current.
- `sitemap.xml` `lastmod` is recent; `robots.txt` allows all + points to sitemap.
- `llms.txt` matches the business facts above.
- Reminder: the real Google Search Console token replaces
  `REPLACE_WITH_YOUR_GSC_VERIFICATION_TOKEN` (one-time; flag until done).

## Step 3 — Rotate the hotel focus

Pick **2 hotels** from `growth/hotel-outreach-kit.md` that were NOT the focus
last week (see the tracker). This week's content and outreach lead with those
two (e.g. "5 minutes from Sheraton Grand" / "delivered to your voco room").

## Step 4 — Write the week's social posts (hotel-guest angle)

Produce **3 posts** ready to publish (Instagram / TikTok caption + Facebook),
each in **English and Arabic**, each with the WhatsApp CTA (+971 54 781 6266):
1. "Staying at [hotel A]? Authentic Damascus food, 5 min away, open till 5 AM."
2. Signature-dish hero (mansaf / mixed grill / manakish) + "delivered to your
   hotel room on Sheikh Zayed Road."
3. Late-night hook ("WTC late shift / after the exhibition — we're open till 5 AM").

Use 8–12 local hashtags (#SheikhZayedRoad #DowntownDubai #DubaiFoodie
#SyrianFood #DWTC #TradeCentreDubai …). Keep on-brand: warm, Damascene, premium.

## Step 5 — Concierge outreach drafts

From the kit, draft outreach for this week's 2 focus hotels:
- A short **WhatsApp/DM** message to the concierge/guest-services desk.
- A short **email** version.
Offer: late-night authentic Syrian for their guests, fast delivery to rooms,
private/group dining and a concierge referral card. Include menu PDF link and
WhatsApp. Keep it warm, specific, one ask. (Templates in the kit.)

> These are **drafts for a human to send** — do not contact hotels
> automatically. Surface them in the summary for approval.

## Step 6 — Google Business Profile + KPI log

- One GBP post idea for the week (offer/dish/late-night/hotel-guest angle).
- Append a dated row to `growth/weekly-log.md`:
  `date | queries won/total | focus hotels | posts drafted | outreach drafted | notes`

## Step 7 — GM summary

Output a tight summary to chat:
- Visibility: X/6 money queries won (and which are missing)
- This week's 2 focus hotels
- 3 social posts (EN+AR) — ready to publish
- 2 concierge outreach drafts — ready to send
- GBP post idea
- Top 1–2 actions for a human (e.g. "add GSC token", "reply to new Google review")

Keep the chat summary short; the posts/outreach are the deliverable.

---

### Notes for whoever schedules this
- Designed to run **every Friday morning** as a scheduled Claude Code (web)
  session. The trigger prompt can simply be: `Run /shamiat-friday`.
- Read-only by default (search + draft). It does **not** post to social or
  message hotels on its own — a human approves and sends.
- If on-site drift is found in Step 2, fix it on the working branch and open a
  PR rather than editing production directly.
