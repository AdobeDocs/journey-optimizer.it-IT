---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---
# Turno di verifica — il controllo di qualità finale obbligatorio

Questo è il gate 2 di 2 e il passaggio che garantisce che ogni blocco sia **valido, vero e privo di
ambiguità&#x200B;**. &#x200B;** non è facoltativo e non può essere saltato**, incluso per gli aggiornamenti a pagina singola.

## Perché è separato

L&#39;autore del blocco (gate 1) è troppo vicino al blocco per rilevare i propri errori di messa a terra. Gate 2
è un **controllo avverso indipendente**: un nuovo revisore che presume che il blocco sia errato
e prova a dimostrarlo, utilizzando **solo** il corpo della pagina come verità. Eseguilo come **subagent separato**
che non ha visto come è stato scritto il blocco — questa indipendenza è ciò che lo rende efficace. Per
un batch di pagine, un subagent di verificatore può coprire l&#39;intera cartella.

## Funzionamento del verificatore per pagina

1. Leggi la **pagina sorgente completa** `help/using/<folder>/<page>.md`. HTML-comment /
il contenuto con commento esterno è **non** origine valida.
2. Leggi il **blocco** `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`.
3. Classifica **ogni** attestazione come FONDATA / INESATTA / NON-FONDATA rispetto al corpo della pagina.
4. **Risolvere ogni problema modificando solo il file di blocco**. Mantenere le due aperture corrette
paragrafi, i limiti `+++ … +++` e il commento di sincronizzazione. Non modificare mai la pagina sorgente.
5. Report per pagina: `clean` o `N issues` + le correzioni applicate.

## L&#39;elenco di controllo degli avversari (prima gli articoli più rischiosi)

- **Numeri e limiti.** Ogni valore esatto. Un limite è `(hard limit)` solo se la pagina utilizza
imposizione/formulazione massima; `(default)` se razionabile/predefinita/configurabile (inclusa &quot;richiesta&quot;)
altri tramite il rappresentante Adobe&quot; o &quot;raisable via API&quot;); `(recommended)` per consigli; no
qualificatore se la pagina non fornisce alcun. **Abbassare di livello qualsiasi tappo del generatore sovraetichettato come rigido.**
Ogni valore di velocità effettiva/velocità effettiva ha il suo ambito.
- **Date, ID, nomi di prodotti/campi, identificatori SQL, enum di stato, stringhe di errore** — testo letterale
dalla pagina. Tolleranza zero su tempi legali e di conformità: mai inventare un SLA, conservazione,
o data di applicazione; mantieni qualsiasi data esattamente come la pagina lo indica ed etichettata come la pagina
lo inquadra.
- **Sinonimi e non confondere.** Un sinonimo (`"A" = "B"`) richiede entrambi i moduli nella pagina
significa la stessa cosa. Qualsiasi contrasto (`"X" ≠ "Y"`) appartiene a &quot;Non confondere&quot;. Sposta
etichette errate.
- **Modalità di convalida/test** denominate con i termini esatti della pagina, non unite
esperienze classiche o riprogettate per diversi canali.
- **Messa a terra.** Niente importato da un&#39;altra pagina, informazioni generali sul prodotto o un HTML
commento. Rimuovere gli elementi non supportati dal corpo della pagina.
- **Stile.** Nessuna contrazione (al di fuori delle stringhe `[!UICONTROL ...]` / `[!DNL ...]`). None (Nessuno)
delle parole vietate (&quot;sintetico&quot;, &quot;dati falsi&quot;, &quot;senza dati reali&quot;, &quot;ripristina&quot;, &quot;ripristina indietro&quot;)
a meno che non sia riportato alla lettera sulla pagina. Le stringhe dell’interfaccia utente vengono mantenute esattamente.
- **Struttura.** Due paragrafi di apertura fissi intatti e testuali; sei sezioni presenti e in
ordina dove la pagina li supporta; sincronizza commento presente.

## Prompt agente secondario verificatore riutilizzabile

Compila la cartella e l’elenco delle pagine. Avviarlo come subagent indipendente per scopi generali.

```
You are an ADVERSARIAL fact-checker for Adobe Journey Optimizer doc "AI Knowledge Reference"
blocks. Repo: <repo path>. Assume each block MAY contain errors; try hard to find them. This is
the final accuracy gate.

PAGES (basenames): <p1> <p2> ...
SOURCE: help/using/<folder>/<p>.md   BLOCK: help/_includes/do-not-localize/<folder>/ai-augmented-<p>.md

For EACH page:
1. Read the FULL source page body (HTML-comment / commented-out content is NOT valid source).
2. Read the block.
3. Classify EVERY claim GROUNDED / INACCURATE / NOT-GROUNDED against the page body. Scrutinize:
   numeric limits (hard only if the page uses enforcement/maximum wording; downgrade any
   raisable/default/configurable value the block marked hard; every rate figure needs its
   scope); dates/IDs/field names/SQL identifiers/status enums/error strings verbatim and no
   invented SLA/legal timeframes; Synonyms are true equivalents (mislabels -> Do not confuse);
   validation/test modes named with the page's exact terms and not conflated; nothing imported
   from other pages or HTML comments; no contractions (outside verbatim [!UICONTROL ...]); no
   banned words (synthetic / fake data / without real data / revert / roll back) unless verbatim.
4. FIX every issue by editing ONLY the block file. Preserve the two fixed opening paragraphs,
   the +++ ... +++ fences, and the sync comment. Do NOT modify source pages.

Report per page: "<p>: clean" or "<p>: N issues" + the exact fixes applied.
```

## Criteri di uscita

La cartella supera il gate 2 solo quando il verificatore segnala ogni pagina come `clean` (è stato trovato
niente, oppure sono state applicate correzioni e il blocco è ora pulito). Se ha applicato le correzioni, sono già
nei file di blocco: includili nel rapporto finale e procedi alla sweep e al commit.
