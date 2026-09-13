---
name: ai-augmented-blocks
description: Genera e gestisci blocchi di riferimento di conoscenza IA per la documentazione di Adobe Journey Optimizer (percorsi-optimizer.en). Utilizzare quando una nuova pagina in aiuto/utilizzo/richiede un blocco di IA, quando una pagina esistente viene modificata e il relativo blocco può essersi spostato, oppure quando viene richiesto di aggiungere/aggiornare/verificare il contenuto di Riferimento della Knowledge Base di AI (AI-augmented). Produce un file do-not-localize include in help/_include/do-not-localize/<folder>/ai-augmented-<page>.md, lo collega alla pagina con {{$include}}, esegue un ciclo di verifica indipendente obbligatorio in modo che il blocco sia vero e non ambiguo, tiene traccia del lavoro in un'attività DOCAC JIRA e (solo dopo aver richiesto all'autore) apre una PR. NON unisce MAI.
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 0%

---


# Blocchi di riferimento della conoscenza di IA

Questa abilità genera e mantiene **Riferimento conoscenza IA** blocchi pannello a soffietto per
Documentazione di Adobe Journey Optimizer (`journey-optimizer.en`). I blocchi sono strutturati,
contesto non localizzato aggiunto alle pagine della documentazione in modo che l’Assistente AI risponda alle domande su
Journey Optimizer in modo più preciso.

Ogni blocco viene archiviato come **include-do-not-localize** (quindi non viene mai tradotto) e estratto
nella pagina con `{{$include}}`. Un blocco contiene **solo fatti derivabili dalla propria pagina
body**: nessun elemento importato da altre pagine, informazioni generali sul prodotto o commenti HTML.

> **Leggere i file di riferimento prima di generare qualsiasi elemento.** Contengono le regole effettive, non
> una sintesi:
> - `references/generation-spec.md` — struttura a blocchi, apertura fissa, sezione per sezione
>   regole di contenuto e ogni regola di precisione (limiti rigidi o consigliati, modalità di convalida,
>   etichette di stato, nessuna contrazione, elenco di parole non consentite).
> - `references/verification-round.md` — verifica dei fatti in contraddittorio **obbligatorio** indipendente
>   questo è il gate di qualità finale. Questo non è facoltativo e non può essere saltato.
> - `references/git-jira-tracking.md` — ramo/commit/flusso PR (chiedere all&#39;autore prima di aprire un
>   PR; **non unire mai**) e il tracciamento DOCAC JIRA.

## Quando si applica questa abilità

- **La nuova pagina** è stata creata in `help/using/<folder>/` → generare un blocco.
- **La pagina esistente è cambiata** → verificare se il blocco è stato spostato dal corpo della pagina e aggiornarla.
- È stato chiesto di **aggiungere, aggiornare, verificare o controllare** blocchi con IA di riferimento o potenziamento della Knowledge Base.

## Ambito di applicazione ed esclusioni

- **Nell&#39;ambito:** pagine in `help/using/<folder>/`.
- **Escluso dall&#39;ambito. Non aggiungere mai blocchi qui:**
  - `help/rp_landing_pages/` (get-started/landing pages) — escluso dalla regola di authoring.
  - Hub di navigazione/collegamento thin, pagine di solo indice e pagine quasi vuote. Quando una pagina è vuota
    elenco di collegamenti privi di concetti sostanziali, **saltarlo e spiegare perché** — non forzare un blocco.
  - Note sulla versione (`help/using/rn/`, pagine note sulla versione).
- In caso di dubbi sulla validità di una pagina, giudicate in base al contenuto: se insegna vero
i concetti, i vincoli o la terminologia coprono il problema; se punta solo altrove, saltalo.

## Flusso di lavoro

**una cartella (o una pagina) alla volta**. Non creare batch di cartelle non correlate in un ramo.

### 1 — Determinare i target e la modalità

Chiedi all’autore (o deduci dalla richiesta/apri file) quali pagine elaborare, e rileva
modalità per pagina:

- **CREA** — la pagina non contiene `{{$include .../ai-augmented-<page>.md}}` righe e non esiste
blocco `+++ AI Knowledge Reference` in linea → generare un nuovo blocco.
- **UPDATE** — la pagina contiene già un blocco. Calcola l’hash page-body e confrontalo con il
  `source-hash` nel commento di sincronizzazione dell&#39;inclusione (vedere di seguito). Se si differenziano, la pagina si →
  rigenera/aggiorna il blocco. Se corrispondono, il blocco è corrente → salta (rapporto &quot;aggiornato&quot;).
- **MIGRATE** — la pagina contiene un blocco *inline* `+++ AI Knowledge Reference` (non ancora
esternalizzato) → spostarlo in un&#39;inclusione do-not-localize e sostituirlo con il `{{$include}}`
linea, mantenendo la fedeltà del contenuto.

Calcola l’hash del corpo della pagina nello stesso modo ovunque (utilizzato per il commento di sincronizzazione e il controllo della deriva):

```bash
md5 -q help/using/<folder>/<page>.md | cut -c1-8
```

Calcola **prima** della modifica della pagina (l&#39;hash copre il corpo così come è quando il blocco è
generate). Su Linux utilizzare `md5sum help/using/<folder>/<page>.md | cut -c1-8`.

### 2 — Genera (o aggiorna) il blocco

Segui `references/generation-spec.md` esattamente per ogni pagina. Invarianti chiave:

- Due **paragrafi di apertura corretti**, letterali, byte per byte (mai parafrasati).
- Sezioni nell&#39;ordine: **TL;DR, Intenti, Glossario, Guardrail, Terminologia, FAQ**.
- Ogni richiesta di risarcimento si è basata solo sul corpo della pagina. Nessuna contrazione. Qualifica numeri come
  `(hard limit)` / `(recommended)` **only** quando la pagina utilizza imposizione/consigli
  testo; altrimenti nessun qualificatore. Utilizza le etichette di stato e modalità di convalida esatte della pagina.
  Mantieni le stringhe `[!UICONTROL ...]` / `[!DNL ...]` nel testo. Non utilizzare mai il carattere impreciso vietato
  termini a meno che non vengano visualizzati letteralmente sulla pagina.

**Includi file** — `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`
(creare la sottodirectory `<folder>` se necessario; appiattire qualsiasi percorso di pagina nidificata con `-`):

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening paragraphs + the six sections]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of the page body> -->
```

**Modifica pagina** — aggiungi esattamente una riga, come ultima riga di contenuto, preceduta da una riga vuota
(non toccare altri elementi nella pagina):

```
{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}
```

Al momento dell&#39;aggiornamento, modificare solo il file di inclusione (e il bump `ai-section-version` se si desidera tenere traccia di
revisioni); la riga `{{$include}}` della pagina in genere rimane la stessa. Aggiorna `source-hash` in
l’hash pagina-corpo corrente una volta che il blocco corrisponde nuovamente alla pagina.

Esegui l&#39;**autocontrollo** in `references/generation-spec.md` (passaggio 3 verifica-ogni-attestazione + la
checklist di post-generazione) prima di procedere. Questo è il cancello 1 di 2.

### 3 — Turno di verifica indipendente (cancello finale obbligatorio)

Questo è il passaggio che l&#39;autore richiede specificatamente: **conferma che ogni blocco sia valido, vero e
senza ambiguità.** Esegui come *passaggio indipendente*, idealmente un subagent separato che
visualizza solo il corpo della pagina e il blocco, senza alcun ricordo di come è stato scritto il blocco, seguendo
`references/verification-round.md`. Ricontrolla ogni richiesta, abbassa qualsiasi limite etichettato in modo errato,
corregge gli errori Synonyms-vs-Do-confuse e rimuove tutto ciò che non è messo a terra nella pagina. Applica
ogni correzione al file include prima di continuare. Questo è il gate 2 di 2 e non può essere saltato.

### 4 — sweep strutturale

Prima di eseguire il commit, eseguire lo sweep di ogni blocco per la struttura e l&#39;igiene (vedere lo snippet di sweep in
`references/git-jira-tracking.md`): materia prima + `# AI Knowledge Reference` intestazione, il
`+++ … +++` recinzioni, il paragrafo di apertura fisso, il commento di sincronizzazione, nessuna contrazione (escluso
verbatim `[!UICONTROL ...]`) e una riga `{{$include}}` corrispondente nella pagina.

### 5 — Traccia in JIRA, poi chiedi di una PR (mai unione)

`references/git-jira-tracking.md`:

1. Eseguire il commit di un ramo denominato per l&#39;attività JIRA (`DOCAC-<key>`), mai in `main`. Verificare la
commit terminato sul ramo (1 commit prima di `origin/main`), non su `main`.
2. Aggiorna l’attività DOCAC: commenta con ciò che è stato modificato + il risultato della verifica, imposta la correzione
e la transizione secondo le esigenze del processo del team.
3. **Chiedi all&#39;autore se desidera una richiesta di pull.** Aprine uno solo se dicono di sì.
4. **Non unire mai.** Queste PR sono per revisione umana; l&#39;unione è sempre la chiamata dell&#39;autore.

### 6 — Relazione

Report per pagina: creato/aggiornato/migrato/ignorato (+ motivo), il risultato della verifica
(pulita o corretta, con le correzioni), l’attività JIRA e il collegamento PR, se presente.

## Note per gli autori che eseguono questa abilità

- Il blocco è un **derivato del corpo della pagina in un determinato momento**. Consideralo come parte del
pagina. Quando modifichi una pagina in modo da toccare un guardrail, un limite, un’etichetta di stato o
modalità di convalida, aggiorna il blocco con la stessa modifica.
- Le fasi JIRA e PR devono poter accedere al JIRA aziendale e a GitHub. Se non ne hai uno
accedi, genera comunque + verifica il blocco e apri la modifica localmente; passa i passaggi JIRA/PR
a qualcuno che lo fa.
- Questa abilità risiede nell’archivio, quindi l’intero team di scrittura condivide un processo. Migliorare
fare riferimento ai file anziché conservare copie private.
