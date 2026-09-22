# Cosa usare

Obbligatori. Senza questi due la lista è un’opinione.

## 1. Google Keyword Planner

- Serve un account **Google Ads** (anche senza campagne attive).
- Imposta località (Italia, o città se l’attività è locale) e lingua.
- Parti dai semi del prodotto; usa «Scopri nuove parole chiave» e, se serve, «Inizia con un sito» sul dominio del cliente (per vedere come Google lo legge, non per copiare i competitor a occhio).
- Prendi: volume medio, andamento 12 mesi, idee collegate. Ordine di grandezza, non la cifra esatta.
- **Non usare:** colonna Competition, CPC, «impressioni in cima» come prova organica. Sono asta ads.
- Overlay di ad-block (uBlock, Ghostery, Disconnect) coprono i grafici: nascondili da JS/CSS sulla pagina Planner, non far disinstallare le estensioni.

Alternative ammesse solo se il Planner è chiuso: Autocomplete Google, «Le gente chiede anche», ricerche correlate. Non sostituiscono il volume. Tool SEO a pagamento (Semrush, Ahrefs, Ubersuggest) sono un di più; se i numeri divergono, vince il Planner + la SERP vera.

## 2. Google organico, da persona

- Incognito (o finestra senza login).
- Località coerente col Planner (stesso Paese; se è locale, stessa città).
- **Le ads in cima e lo Shopping non si contano.** Scorri i risultati organici: i 10 blu, il pack Maps, i video, i sitelink.
- Apri 3–5 URL in cima: che pagina è (guida, prodotto, directory, scheda Maps, homepage)? Quanto è specifica? Data? Zona sbagliata?

Search Console e Bing servono **dopo**, su pagine già pubblicate. Non per scoprire keyword nuove se il sito non ha traffico.

## Strada consigliata e alternativa

Stesso lavoro, due porte. Se l'MCP è collegato, usalo. Se non c'è, **browser-use** copre le stesse schermate: costa più token e si rompe più spesso (overlay, quota, incolla storto), ma per poche URL il risultato è lo stesso.

| Cosa | Consigliato (MCP) | Alternativa |
|---|---|---|
| Volumi e idee | Keyword Planner via Google Ads (`google-keyword-planner-mcp`). Competition e CPC sono ads, ignorali. Il token Ads nuovo sta in prova finché Google non approva il Basic: nel frattempo solo browser. | browser-use sul Planner, account Ads già loggato. Nascondi l'overlay degli ad-block, non farli disinstallare. |
| SERP organica | Nessun MCP sostituisce l'occhio. | browser-use, finestra senza login, ads e Shopping ignorati. |
| «È in Google?» query, click, posizione | Search Console (`mcp-google-search-console`). L'API **ispeziona**, non preme «Richiedi indicizzazione». | browser-use su Search Console. Il bottone di richiesta si preme solo qui. Poche URL al giorno. |
| Invio URL e crawl per ChatGPT/Copilot | Bing Webmaster (`bing-webmaster-mcp`), chiave API. L'URL deve coincidere con quella registrata, slash compreso. | browser-use su Bing Webmaster. Non risottomettere una sitemap già in Success. |

Non collegare gli MCP se le pagine nuove sono poche: il browser basta. Collegali quando rileggere Search Console a mano diventa il lavoro.

## Link

Credenziali (application password, chiavi API, token) restano in locale. Non vanno nel repo.

| Uso | Link |
|---|---|
| Browser, alternativa a tutti i pannelli | [browser-use](https://github.com/browser-use/browser-use) |
| Pagine Elementor su WordPress (`npx elementor-mcp`) | [Elementor-MCP](https://github.com/aguaitech/Elementor-MCP) |
| WordPress oltre Elementor: post, media, meta (Yoast), redirect. Application password, non la password di login | [REST WordPress, application password](https://developer.wordpress.org/rest-api/using-the-rest-api/authentication/#application-passwords) |
| MCP WordPress generico, se il sito non è fatto in Elementor | [mcp-wordpress](https://github.com/docdyhr/mcp-wordpress) |
| Volumi | [Keyword Planner](https://ads.google.com/home/tools/keyword-planner/) · MCP [google-keyword-planner-mcp](https://github.com/ncosentino/google-keyword-planner-mcp) |
| «È in Google?», query, click, posizione | [Search Console](https://search.google.com/search-console) · MCP [searchconsole-mcp](https://github.com/chrishart0/searchconsole-mcp) |
| Bing, invio URL, ChatGPT/Copilot | [Bing Webmaster](https://www.bing.com/webmasters) · MCP [bing-webmaster-mcp](https://github.com/idowebid/bing-webmaster-mcp) |

Su un sito Elementor la pubblicazione delle pagine è Elementor-MCP. Yoast, redirect e tutto ciò che non è il builder passano dalla REST di WordPress. browser-use copre Planner, SERP, Search Console e Bing se l'MCP non è collegato. Il bottone «Richiedi indicizzazione» esiste solo nel browser.

## Non usare come fonte

- Liste keyword generate da un modello (questa skill inclusa) senza Planner e SERP.
- Volume da un tool solo, senza aprire Google.
- Keyword stuffing per un plugin SEO (pallino verde Yoast e simili).
