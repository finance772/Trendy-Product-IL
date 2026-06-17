---
name: kbeauty-product-links
description: >
  Refresh / rebuild the Korean (K-Beauty) products popup in index.html so that
  every product has two working links: a purchase link to an active official
  retailer, and a link to its most successful viral promotion source. Also
  splits the products into "already available in Israel" vs "new / not yet in
  Israel". Use when the user asks to update, refresh, re-run, or rebuild the
  K-Beauty product links / popup. Triggers: "רענן את הלינקים של הקוריאנים",
  "עדכן מוצרים קוריאניים", "הרץ מחדש את הסקיל של ה-K-Beauty", "תוסיף לינקים
  למוצרים קוריאנים", "update k-beauty links", "refresh korean products",
  "re-run kbeauty skill", "rebuild k-beauty popup".
---

# K-Beauty Product Links

Maintains the Korean skincare (K-Beauty) popup inside `index.html` of the
Trendy-Product-IL dashboard. Each Korean product gets **two links**:

- 🛒 **רכישה (Purchase)** — to an *active, official* retailer that ships to Israel.
- 📣 **פרסום (Promotion)** — to the product's most successful viral source
  (TikTok), the content that turned it into a trend.

The products are split into two columns:

- 🟢 **כבר זמינים בישראל** — products already sold in Israel.
- 🔴 **טרנדים חדשים / עתידיים** — trending products that have **not yet**
  arrived in Israel (keep this column at **4 products**).

## When to run

Run whenever the user asks to update / refresh / re-run / rebuild the K-Beauty
product links or popup (Hebrew or English). The goal each run is a fresh,
correct, fully-linked popup.

## Steps

1. **Open `index.html`** and locate:
   - the `kbeautyLinks` map (top of the `<script>`), which holds `{ buy, ad }`
     URLs per product name;
   - the `kbeautyItem(name)` helper that renders one product row;
   - the `openKBeautyDashboard()` function, which contains the two `<ul>` lists
     (the "כבר זמינים בישראל" column and the "טרנדים חדשים / עתידיים" column).

2. **Decide the product list.** Keep the established products in the
   "available in Israel" column. For the "not yet in Israel" column, pick **4**
   genuinely-trending K-Beauty products that are not yet sold in Israel.
   - If web access is available, verify current trends and Israeli availability
     before choosing. If not, choose from current knowledge and **clearly warn
     the user** that availability was not verified live and should be checked
     before publishing.

3. **Categorise correctly.** A product belongs in "כבר זמינים בישראל" if it is
   actually sold in Israel (e.g. linkable to iHerb Israel / Super-Pharm / a
   local store). Otherwise it goes in the "new / not yet in Israel" column.

4. **Set the links** in the `kbeautyLinks` map:
   - **Purchase link** must resolve to a *working* page on an active retailer:
     - Available-in-Israel products → `https://il.iherb.com/search?kw=<PRODUCT>`
     - Not-yet-in-Israel products → `https://www.amazon.com/s?k=<PRODUCT>`
       (Amazon ships to Israel and sells these brands officially).
     - **Avoid known-broken search formats** (e.g. YesStyle
       `?q=` returned "Page Not Available"). Prefer stable search URLs over
       direct product-page URLs, which break when stores change paths. Only use
       a direct product/official-store URL if the user provides it.
   - **Promotion link** → `https://www.tiktok.com/search?q=<PRODUCT>` (or a
     specific viral video URL if the user provides one).
   - URL-encode product names (spaces → `%20`, or `+` for Amazon).

5. **Render the columns** by calling `kbeautyItem("<name>")` for each product in
   the correct `<ul>` inside `openKBeautyDashboard()`.

6. **Keep the copy clean:**
   - Use regular hyphens `-` only — **no em-dashes `—` or en-dashes `–`** anywhere.
   - Update the product counts in the description, the legend line, the button
     subtitle, and the modal subtitle so they match the real totals.
   - The legend should state which retailer each column links to.
   - Do **not** show the static "למה זה כדאי לחנות אונליין?" heading in the
     K-Beauty popup (it is hidden via `whySection`); keep it only for regular
     product details.

7. **Verify** no em/en dashes remain (e.g. `grep -c "—" index.html` and
   `grep -c "–" index.html` should both be 0) and that every product in both
   columns has an entry in `kbeautyLinks`.

8. **Commit and push** to the working branch with a clear message, then send the
   updated `index.html` to the user and remind them they can drag-and-drop it to
   Netlify (project `trendydrodil`) to publish.

## Current state (reference)

🟢 **כבר זמינים בישראל (iHerb Israel links):** COSRX Snail Mucin · Beauty of
Joseon · Anua Heartleaf · Haruharu Wonder · Medicube Collagen Jelly · VT
Cosmetics Reedle Shot · Torriden Dive-In Serum · Abib Heartleaf

🔴 **טרנדים חדשים / עתידיים (Amazon links, 4):** Tirtir Mask Fit Red Cushion ·
Kahi Wrinkle Bounce Multi Balm · ma:nyo Pure Cleansing Oil · Mixsoon Bean Essence

📣 All promotion links point to a TikTok search for the product.

## Notes & gotchas

- This environment's network egress may block the live site and external
  retailers, so links usually can't be fetched/verified from here — say so when
  relevant instead of claiming a link was tested.
- The deployed site is a **manual drag-and-drop** Netlify deploy
  (project `trendydrodil`); it is not auto-built from this repo, so the user
  must re-upload `index.html` to publish (or connect the repo to Netlify).
