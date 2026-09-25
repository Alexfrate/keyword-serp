# What to use

Two sources are mandatory. Without them the list is an opinion.

## 1. Google Keyword Planner

- You need a **Google Ads** account (campaigns can be off).
- Set location (country, or city if the business is local) and language.
- Start from product seeds. Use "Discover new keywords" and, if useful, "Start with a website" on the customer's domain (to see how Google reads it, not to copy competitors by eye).
- Take average volume, the 12-month trend, and related ideas. Order of magnitude, not the exact figure.
- **Do not use** the Competition column, CPC, or "top of page bid" as organic proof. That is the ad auction.
- Ad blockers (uBlock, Ghostery, Disconnect) cover the charts. Hide the overlay. Do not tell the user to uninstall them.

If Planner is blocked, Google Autocomplete, "People also ask", and related searches are allowed. They do not replace volume. Paid SEO tools (Semrush, Ahrefs, Ubersuggest) are extra. If the numbers disagree, Planner plus the live SERP wins.

## 2. Organic Google, as a person

- Logged out, or a window without a Google account.
- Same place as Planner (same country; same city if it is local).
- **Ads at the top and Shopping do not count.** Read the organic results: the ten blue links, the Maps pack, videos, sitelinks.
- Open 3 to 5 URLs at the top. What kind of page is it (guide, product, directory, Maps listing, homepage)? How specific? How old? Wrong city?

Search Console and Bing come **after**, on pages that are already published. They do not discover new keywords on a site with no traffic.

## Path

Read volumes and Search Console from the connected tools. The browser is the fallback, and it stays mandatory only for the SERP (logged out) and for the "Request indexing" button.

| Job | First choice | Browser only if |
|---|---|---|
| Volume and ideas | Google Ads API, the same Keyword Planner methods (`generateKeywordIdeas`, `generateKeywordHistoricalMetrics`). Put geo, language, and the Google search network in the call, or it is not the screen you think you opened. Ignore Competition and CPC: those are ads. | The Cloud project's access is not **Basic** yet. |
| Organic SERP | Nothing replaces looking. | Always: logged out. Ignore ads and Shopping. |
| "Is it on Google?", queries, clicks, position | Search Console MCP. It inspects. It does not press "Request indexing". | For that button. A few URLs a day. |
| Visits, sessions, events | Analytics (GA4) MCP. It counts people who accepted the cookie banner. It does not have the Google query, so it does not pick keywords. | Never, for keywords. |
| Submit a URL for ChatGPT/Copilot | Bing Webmaster, if the API key exists. The URL must match, including the slash. | Until the key exists. Do not resubmit a sitemap that is already Success. |

### What we checked on Planner

[google-keyword-planner-mcp](https://github.com/ncosentino/google-keyword-planner-mcp) calls the same function as the Planner screen. It is not a site that estimates volume. Downloading it is not enough to make it answer.

- Access lives on the Cloud project, not on a developer token (Google turned those off in September 2026). **Test** only talks to fake accounts. **Explorer** refuses volumes with `DEVELOPER_TOKEN_NOT_APPROVED`. You need **Basic**.
- Basic does not pass until the OAuth brand is verified: app name, homepage, privacy policy on an authorized domain, then "Verify branding" and "Publish branding". The verify button shows up only after the app is **In production**, not while it is in Testing.
- Same phrase, Italy, Google search network: the screen shows a dash (or the 0–10 bucket, which is not a real figure). The API returns the phrase and **no** average monthly searches. That is the same fact. Do not reopen the browser to fetch "the real number".
- If you doubt the call is mute, repeat it on a phrase that has volume (for example "web designer" in Italy does). If that one returns a number and yours does not, yours has no number.
- That repo, as published, still requires `GOOGLE_ADS_DEVELOPER_TOKEN` and will not start. The door that works is a direct API call with the OAuth refresh token kept on the machine. Credentials do not go in the repo.

## Links

Credentials (application passwords, API keys, tokens) stay on the machine. They do not go in the repo.

| Job | Link |
|---|---|
| Browser, fallback for every panel | [browser-use](https://github.com/browser-use/browser-use) |
| Elementor pages on WordPress (`npx elementor-mcp`) | [Elementor-MCP](https://github.com/aguaitech/Elementor-MCP) |
| WordPress besides the builder: posts, media, meta (Yoast), redirects. Application password, not the login password | [WordPress REST, application passwords](https://developer.wordpress.org/rest-api/using-the-rest-api/authentication/#application-passwords) |
| Generic WordPress MCP, if the site is not Elementor | [mcp-wordpress](https://github.com/docdyhr/mcp-wordpress) |
| Volume | [Keyword Planner](https://ads.google.com/home/tools/keyword-planner/) · MCP [google-keyword-planner-mcp](https://github.com/ncosentino/google-keyword-planner-mcp) |
| "Is it on Google?", queries, clicks, position | [Search Console](https://search.google.com/search-console) · MCP [searchconsole-mcp](https://github.com/chrishart0/searchconsole-mcp) |
| Bing, URL submit, ChatGPT/Copilot | [Bing Webmaster](https://www.bing.com/webmasters) · MCP [bing-webmaster-mcp](https://github.com/idowebid/bing-webmaster-mcp) |

On an Elementor site, page publishing is Elementor-MCP. Yoast, redirects, and anything that is not the builder go through the WordPress REST API. The browser covers the SERP, the "Request indexing" button, and Bing when the key is missing. It no longer covers volumes or Search Console reads, once those tools are connected.

## Do not use as a source

- Keyword lists generated by a model (including this skill) without Planner and a SERP.
- Volume from a model or a paid tool, without Planner (API or screen) and without the SERP.
- Keyword stuffing to please an SEO plugin (a green Yoast dot and the like).
