---
name: keyword-serp
description: >
  Tells an LLM how to structure an SEO page: pick a query with real demand
  and a weak organic page 1, choose the page type from the SERP, write
  spoken professional copy, then request indexing on that URL. Volumes
  and Search Console come from the connected tools, not the browser. Does
  not promise rankings. Triggers: keywords, keyword research, Planner, SERP,
  low competition, indexing, structure an SEO page.
  Use when the user runs /keyword-serp.
---

# Keyword research (weak organic page 1)

This picks **queries**. It does not build the site. The research is the same on WordPress, Shopify, Next, Webflow, or HTML. The CMS only matters later, for title, H1, and URL.

Open these when you need them:

- `references/tools.md` — what to use. Volumes and Search Console from the connected tools; the browser is the fallback
- `references/reading-the-serp.md` — how to judge competition (not the Planner competition dot)
- `references/indexing.md` — after the page is live: request indexing on that URL, Bing for ChatGPT, indexed is not ranking
- `references/writing-the-page.md` — when you write: weight, table, cards, phone, meta. Do it without being asked again

## Before opening Planner

Ask, if it is missing:

1. What they sell, in one line, and what they do **not** sell.
2. Who searches (owner, consumer, B2B).
3. Area: country, city, or both.
4. Live pages and URLs, so you do not duplicate an intent.

Without 1 you invent keywords. Without 4 you cannibalize.

## Steps

1. **Seeds** from the customer's words, not trade jargon. *brochure site*, *how much does a window cost*, not *digital solutions*.
2. **Keyword Planner** on those seeds, through the API (not the browser, once Basic access is on). Geo = the area in step 3, the right language, Google search network. Last 12 months. Keep volume and related ideas. Ignore Competition and CPC: those are ads, not organic. Detail in `tools.md`.
3. **Organic SERP** for each candidate (logged out, ads ignored). Detail in `reading-the-serp.md`. Volume alone is not enough. The SERP alone is not enough.
4. **Keep** the query if (a) people actually search it, (b) page 1 is beatable or the intent is uncovered, (c) the business can answer without inventing a product.
5. **Drop** it even with high volume if the top results are directories, Wikipedia, Amazon, newspapers, a Maps pack (and you are not local), or an intent you do not sell.
6. **Page format comes from the SERP**, not from a fixed rule:
   - guides / "how much" / "how to" → question page (H1 = the query)
   - products → product page
   - Maps + reviews → local listing, not an article
   - brand / company name → home or catalog
   - comparisons / alternatives → versus page or price list
7. **One query (one intent) = one URL.** If that intent already has a page, rewrite that page.

## Output (before writing a line of the site)

For each kept query:

| Query | Volume (order of magnitude) | SERP type | Page format | URL (existing or new) | Why page 1 is weaker |
|---|---|---|---|---|---|

Plus a **do not** list: volume, but an unbeatable SERP or outside what you sell.

Do not promise rankings. This skill chooses *where* to play.

## Copy, when you write the page

Register: **spoken and professional**, in the reader's language. Not an agency brochure (*tailored, by your side, team of experts*), and not sloppy chat. The reader is a customer, not an SEO colleague.

Content rules:

- No invented clients, reviews, numbers, or case studies. Label demos as demos.
- Prices only if they are the real ones, or "from…" if that is the offer.
- The first answer on the page is closed: what it is, what it is not, the price if there is one, how to get in touch. Then the rest.
- The rest of the method (weight against page 1, the table, cards with no holes, phone, meta put back after save) is in `references/writing-the-page.md`. Apply it without waiting to be asked.

For Italian pages, run the copy through an Italian humanizer before publishing. Do not paste model prose.

## Gotchas

- Planner "Competition" = ads. The competition that matters is who owns organic page 1.
- uBlock, Ghostery, and Disconnect cover the Planner charts: hide the overlay, do not ask anyone to uninstall them.
- A question H1 only if the SERP is already questions and guides. Otherwise it sounds wrong.
- A head term (for example *how much does a website cost*) can be the hub even when it is hard. It is not "low competition". Next to it, pick the weaker branches of the same group.
- The page has to match the SERP intent (you do not beat a tax SERP with a shop page).
- Indexed is not ranking. ChatGPT copies whoever is already on the SERP, later.

## After the page is live

Follow `references/indexing.md`. Short version: request indexing on that URL only (the button is in the browser), submit the same URL on Bing, do not resubmit a sitemap that is already Success. Indexed is not page 1.

How you save the page (Elementor, Yoast, Shopify, Next) depends on the CMS. Links are in `references/tools.md`.
