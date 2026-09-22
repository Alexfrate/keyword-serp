# Indexing

Do this after the page is live. It does not create rankings. It asks Google and Bing to fetch that URL.

MCPs are optional. browser-use on Search Console and Bing Webmaster does the same job and spends more tokens (every screen is a long turn, and the UI breaks: overlays, quota, a bad paste).

## Google

1. Search Console, URL inspection, **that URL only**. A few a day. The quota is small.
2. Press **Request indexing**. The API and the MCP only inspect. They do not press the button. That click is in the browser.
3. "URL is on Google" means a copy is in the index. It does not mean page 1.
4. The live test is not the indexed copy. If you change the page, request that URL again. Do not resubmit the whole site.

## Bing

ChatGPT and Copilot read Bing, not Search Console.

1. Bing Webmaster, submit **that URL**.
2. The URL must match the registered one, including the trailing slash.
3. If the sitemap is already Success, do not submit it again.

## After

Wait. In 7 to 10 days, logged out, search the real query. Indexed is not ranking.

Maps and directories come later, and only if Google still does not show the page. They are not part of this step.
