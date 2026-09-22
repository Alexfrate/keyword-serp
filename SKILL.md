---
name: keyword-serp
description: >
  Pick keywords with real demand and a weak organic page 1, then say what
  page type to build. Copy, if written, is spoken and professional: no
  agency brochure, no invented clients. Does not publish the site. Uses
  Keyword Planner plus the organic Google results (ads do not count).
  Triggers: keywords, keyword research, Planner, SERP, low competition,
  search intent, H1, what people search.
  Use when the user runs /keyword-serp.
---

# Keyword research (weak organic page 1)

This picks **queries**. It does not build the site. The research is the same on WordPress, Shopify, Next, Webflow, or HTML. The CMS only matters later, for title, H1, and URL.

Open these when you need them:

- `references/tools.md` — what to use, with links: Planner, Search Console, Bing, browser-use, Elementor-MCP, WordPress REST
- `references/reading-the-serp.md` — how to judge competition (not the Planner competition dot)

## Before opening Planner

Ask, if it is missing:

1. What they sell, in one line, and what they do **not** sell.
2. Who searches (owner, consumer, B2B).
3. Area: country, city, or both.
4. Live pages and URLs, so you do not duplicate an intent.

Without 1 you invent keywords. Without 4 you cannibalize.

## Steps

1. **Seeds** from the customer's words, not trade jargon. *brochure site*, *how much does a window cost*, not *digital solutions*.
2. **Keyword Planner** on those seeds. Geo = the area in step 3. Last 12 months. Keep volume and related ideas. Ignore the Competition column: that is ads, not organic. Detail in `tools.md`.
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

For Italian pages, run the copy through an Italian humanizer before publishing. Do not paste model prose.

## Gotchas

- Planner "Competition" = ads. The competition that matters is who owns organic page 1.
- uBlock, Ghostery, and Disconnect cover the Planner charts: hide the overlay, do not ask anyone to uninstall them.
- A question H1 only if the SERP is already questions and guides. Otherwise it sounds wrong.
- A head term (for example *how much does a website cost*) can be the hub even when it is hard. It is not "low competition". Next to it, pick the weaker branches of the same group.
- The page has to match the SERP intent (you do not beat a tax SERP with a shop page).
- Indexed is not ranking. ChatGPT copies whoever is already on the SERP, later.

## Out of scope

Publishing (Elementor, Yoast, Shopify metafields, Next `metadata`) and the engines (Search Console, Bing, Maps) are the next step. This skill stops at the table. Tool links for that next step are in `references/tools.md`.
