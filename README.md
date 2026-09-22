# keyword-serp

Pick queries people actually search, where the organic page 1 is weak, then match the page type to that SERP. Works on WordPress, Shopify, Next, Webflow, or plain HTML. It does not promise rankings.

The skill is `SKILL.md`. Details are in `references/`.

## Tools

| Job | Link |
|---|---|
| Browser, fallback for every panel | https://github.com/browser-use/browser-use |
| Elementor pages on WordPress | https://github.com/aguaitech/Elementor-MCP |
| WordPress besides Elementor (REST, application password: Yoast, redirects, posts) | https://developer.wordpress.org/rest-api/using-the-rest-api/authentication/#application-passwords |
| Generic WordPress MCP, if the site is not Elementor | https://github.com/docdyhr/mcp-wordpress |
| Search volume | https://ads.google.com/home/tools/keyword-planner/ · https://github.com/ncosentino/google-keyword-planner-mcp |
| Search Console | https://search.google.com/search-console · https://github.com/chrishart0/searchconsole-mcp |
| Bing (ChatGPT and Copilot) | https://www.bing.com/webmasters · https://github.com/idowebid/bing-webmaster-mcp |

On an Elementor site, pages go through Elementor-MCP (`npx elementor-mcp`). Everything else on WordPress goes through the REST API with an application password. browser-use covers Planner, the SERP, Search Console, and Bing when the MCP is not connected. "Request indexing" exists only in the browser.

No passwords, API keys, or tokens in this repo.
