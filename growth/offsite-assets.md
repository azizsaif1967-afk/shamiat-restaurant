# Shamiat — Off-Site Copy Assets (paste-ready)

These are the things that **can't be pushed from code** — they live in accounts
you control (Google, Instagram, print). Everything below is final copy: just
paste. Complements [hotel-outreach-kit.md](hotel-outreach-kit.md) (concierge/
email templates) — no overlap.

> Single source of truth for facts: Duja Tower, Ground Floor, Sheikh Zayed Road,
> Trade Centre First, Dubai · open daily 12 PM–5 AM · +971 54 781 6266 ·
> 100% halal · Talabat, noon, Keeta, Smiles, Deliveroo, Careem.

---

## 1. Google Business Profile — description
*(GBP → Edit profile → Description. ~750 char limit.)*

```
Shamiat is an authentic Syrian and Levantine restaurant on the ground floor of Duja Tower, Sheikh Zayed Road, Trade Centre First, Dubai — open daily from 12 PM to 5 AM.

We serve cold and hot mezze, charcoal grills, Damascene slow-cooked mains, clay-pot fakhara, manakish, seafood, sweets and fresh juices. 100% halal kitchen.

We are walking distance from the Sheraton Grand Dubai, Novotel & Ibis World Trade Centre, Four Points by Sheraton SZR, Crowne Plaza SZR, Towers Rotana, Fairmont Dubai, voco Dubai, Millennium Plaza, Rove Trade Centre, Dusit Thani, Conrad, Shangri-La and all major Sheikh Zayed Road hotels.

Dine in, reserve a table, or order delivery to your hotel room on Talabat, Deliveroo, noon, Keeta, Smiles or Careem. Group and concierge bookings welcome.
```

**GBP setup checklist (one-time):**
- Primary category: **Restaurant** · add secondaries: Syrian Restaurant,
  Arabic Restaurant, Middle Eastern Restaurant, Lebanese Restaurant.
- Pin the map marker exactly on Duja Tower (25.22885, 55.286282).
- Set hours 12:00 PM–5:00 AM, every day.
- Upload 30–50 of the menu/dish photos already on the site.
- Turn on messaging; link the WhatsApp/menu PDF.
- Ask happy guests to leave a review **mentioning their hotel by name**
  ("came from the Sheraton, best Syrian near DWTC").

---

## 2. GBP weekly posts (rotate one per week)
*(GBP → Add update. Add a photo to each.)*

**Post 1 — Hotel guests**
```
Staying on Sheikh Zayed Road? We're at Duja Tower — a short walk from the Sheraton Grand, Novotel, Ibis, Four Points and 15+ SZR hotels. Authentic Syrian food, open until 5 AM. Order to your room on Talabat or WhatsApp +971 54 781 6266.
```
**Post 2 — Late night**
```
Late-night craving? Shamiat is open until 5 AM every night on Sheikh Zayed Road. Charcoal grills, mezze, mansaf and oze — made fresh to order. Dine in or delivered. Duja Tower, Ground Floor, Trade Centre First, Dubai.
```
**Post 3 — Concierge**
```
Concierges — we'd love to be on your recommended list. Your guests get authentic Syrian & Levantine food, open until 5 AM, a short walk from the hotel. Group bookings welcome. Call or WhatsApp +971 54 781 6266.
```
**Post 4 — Delivery**
```
Delivery across the Sheikh Zayed Road hotel area — Talabat, Deliveroo, noon, Keeta, Smiles, Careem. Or WhatsApp your order: +971 54 781 6266. Shamiat at Duja Tower. Open 12 PM–5 AM daily.
```

---

## 3. Instagram bio
*(Profile → Edit profile. Link: https://shamiatrestaurant.com/)*

```
🍽️ Syrian & Levantine Kitchen
📍 Duja Tower, Sheikh Zayed Road, Dubai
🕐 Open daily 12PM–5AM
🏨 Delivery to all SZR hotels
📞 +971 54 781 6266
🛵 Talabat | Deliveroo | noon | Keeta
```

---

## 4. Concierge card (print — front / back)
*(Business-card or A6 tent card. Drop at every hotel desk within 2 km — target
list in [hotel-outreach-kit.md](hotel-outreach-kit.md). Add a QR code to
https://wa.me/971547816266 on the back.)*

**FRONT**
```
        شاميات · SHAMIAT RESTAURANT
     Authentic Syrian & Arabic Kitchen
        Duja Tower · Sheikh Zayed Road

   ● Open daily 12 PM – 5 AM
   ● Dine in · Table reservations
   ● Delivery to your hotel room
   ● 100% Halal

   📞  +971 54 781 6266
   💬  WhatsApp to order or book
   📍  Minutes from this hotel
```
**BACK**
```
   ORDER DELIVERY TO YOUR ROOM

   1. Open WhatsApp  →  +971 54 781 6266
   2. Send your hotel name + room number
   3. Choose your dishes — we deliver, fast.

   Or order on: Talabat · Deliveroo · noon
                Keeta · Smiles · Careem

   Search: "Shamiat Restaurant"
   shamiatrestaurant.com        [ QR code ]
```

---

## 5. Guest WhatsApp room-order quick reply
*(Save in WhatsApp Business → Quick replies. The live site's "WhatsApp a table
or room delivery" button already pre-fills the customer side of this.)*

```
🍽️ Welcome to Shamiat!

To deliver to your hotel room, please send:
• Hotel name:
• Room number:
• Your order:
• Contact number:

We're open until 5 AM — your food is on the way shortly. 🛵
```

---

## What's already live on the website (no action needed)
- Dedicated **#hotels** section + nav link, 18 hotels listed.
- **4 hotel FAQ entries** + halal FAQ — visible *and* in FAQPage JSON-LD
  (Google AI Overviews / Siri / Alexa read these).
- Meta description, hero, keywords, `llms.txt` all name the SZR hotels.
- Restaurant schema `areaServed` includes the hotels.

## One code TODO that needs YOU
`index.html` line ~16 has a Google Search Console placeholder:
`<meta name="google-site-verification" content="REPLACE_WITH_YOUR_GSC_VERIFICATION_TOKEN">`
→ In Search Console, add property `shamiatrestaurant.com`, copy the HTML-tag
token, paste it in, and re-deploy. Then submit `sitemap.xml`. Until then GSC
data is blind.
