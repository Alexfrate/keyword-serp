---
name: ricerca-keyword
description: >
  Trova parole chiave con domanda vera e SERP organica più debole, poi dice
  che tipo di pagina serve. I testi, se si scrivono, sono italiani parlati e
  professionali (skill scrittura-italiana): niente brochure, niente clienti
  inventati. Non pubblica il sito. Usa Keyword Planner + Google
  organico (le ads non contano). Trigger: parole chiave, keyword, Planner,
  SERP, bassa concorrenza, intent, H1, "che cerca la gente", ricerca keyword.
  Use when the user runs /ricerca-keyword.
---

# Ricerca keyword (bassa concorrenza organica)

Metodo di **scelta delle query**, non di costruzione del sito. Vale su WordPress, Shopify, Next, Webflow, HTML: la ricerca è la stessa. Il CMS entra dopo, per title/H1/URL.

Apri i riferimenti quando servono:
- `references/strumenti.md` — cosa usare, con i link: Planner, Search Console, Bing, browser-use, Elementor-MCP, REST WordPress
- `references/leggere-la-serp.md` — come si misura la concorrenza (non il pallino del Planner)

## Prima di aprire il Planner

Chiedi, se manca:

1. Cosa vende, in una riga, e cosa **non** vende.
2. Chi cerca (titolare, privato, B2B).
3. Zona: Italia, città, o entrambe.
4. Pagine/URL già vive, così non si duplica un intento.

Senza il punto 1 si inventano keyword. Senza il 4 si cannibalizza.

## Procedura

1. **Semi** dalle parole del cliente, non dal gergo del mestiere. *sito vetrina*, *quanto costa un infisso*, non *soluzioni digitali*.
2. **Keyword Planner** su quei semi. Geo = la zona del punto 3. Periodo 12 mesi. Tieni volume e idee collegate. Ignora la colonna «Competition»: è pubblicità, non organico. Dettaglio in `strumenti.md`.
3. **SERP organica** per ogni candidato (incognito, ads ignorate). Dettaglio in `leggere-la-serp.md`. Volume da solo no. SERP da sola no.
4. **Tieni** la query se: (a) qualcuno la cerca davvero, (b) la pagina 1 è battibile o l’intento è scoperto, (c) l’attività può rispondere senza inventare un prodotto.
5. **Scarta** anche col volume alto se in cima ci sono directory, Wikipedia, Amazon, giornali, pack Maps (e non sei locale), o un intento diverso da ciò che vendi.
6. **Formato pagina dalla SERP**, non da una regola fissa:
   - guide / «quanto costa» / «come si fa» → pagina-domanda (H1 = la query)
   - prodotti → scheda prodotto
   - Maps + recensioni → scheda locale, non un articolo
   - marca / nome azienda → home o catalogo
   - confronti / alternative → pagina vs o listino
7. **Una query (un intento) = una URL.** Se l’intento c’è già, si riscrive quella pagina.

## Output (prima di scrivere una riga di sito)

Per ogni query scelta, in tabella:

| Query | Volume (ordine) | Tipo SERP | Formato pagina | URL (esistente o nuova) | Perché è più debole |
|---|---|---|---|---|---|

Più un elenco **non fare**: query con volume ma SERP imbattibile o fuori perimetro.

Non promettere posizioni. Questa skill sceglie *dove* giocare.

## Testi, quando si scrive la pagina

Registro: **italiano parlato e professionale**. Né brochure da agenzia (*su misura, al tuo fianco, team di esperti*), né chat sciatta. Il lettore è un titolare, non un collega SEO.

Prima di stendere o correggere, apri la skill `scrittura-italiana` (umanizza togliendo i tic da AI: perifrasi, triadi, gerundi, «non è X ma Y»). Non duplicarne le regole qui.

Vincoli di contenuto, che quella skill non verifica:

- Niente clienti, recensioni, numeri o casi inventati. Le demo si dichiarano.
- Prezzi solo se sono quelli veri, o «da…» se l’offerta è così.
- La prima risposta della pagina è chiusa: cosa è, cosa non è, quanto costa se c’è un prezzo, come si contatta. Poi il resto.

## Gotcha

- Planner «Competition» = ads. La concorrenza che conta è chi sta in pagina 1 organica.
- uBlock/Ghostery/Disconnect coprono il Planner: nascondi l’overlay, non chiedere all’utente di disinstallare.
- H1-domanda solo se la SERP è già fatta di domande/guide. Altrimenti stona.
- Testa di mercato (es. *quanto costa un sito web*): puoi farla come hub anche se è dura; non è «bassa concorrenza». Accanto, scegli i rami più deboli del gruppo.
- Copy della pagina deve seguire l’intento della SERP (una SERP fiscale non si vince con una scheda WooCommerce).
- Indicizzata ≠ in cima. ChatGPT copia chi è già in SERP, dopo.

## Fuori da questa skill

Pubblicare (Elementor, Yoast, metafield Shopify, `metadata` Next) e motori (GSC, Bing, Maps) sono un altro passo. Qui si ferma alla tabella. Per Lab Creators il cantiere WP sta in `Labcreators/contesto/REGOLE.md`.
