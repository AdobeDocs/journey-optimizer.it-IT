---
source-git-commit: 341538e14ef7de012cce89561727bdecb44d8183
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 0%

---
# augmentedAIContent

Genera un pannello a soffietto **Riferimento conoscenza IA** creato automaticamente per una o più pagine markdown nell&#39;archivio della documentazione di Journey Optimizer e lo memorizza come **elemento di inclusione non localizzato** in modo che non venga tradotto.

## Archivio di destinazione

`help/using/` (relativo alla directory principale dell&#39;archivio)

## Sintassi Accordion (Experience League)

```
+++ AI Knowledge Reference

Content here — any standard markdown is valid.

+++
```

**Regole:**

- `+++ AI Knowledge Reference` apre il Pannello a soffietto (uno spazio dopo `+++`); `+++` da solo su una riga lo chiude
- Riga vuota prima dell&#39;apertura `+++` e dopo la chiusura `+++`
- Il titolo è sempre esattamente `AI Knowledge Reference`

## Includi sintassi (Experience League)

```
{{$include /help/_includes/do-not-localize/<folder>/<include-file>.md}}
```

Il contenuto estratto tramite `{{$include}}` da `help/_includes/do-not-localize/` è **escluso dalla localizzazione**. Il blocco rimarrà non tradotto in questo modo.

&#x200B;---

## Flusso di lavoro

### Passaggio 1 — Richiedi target

Chiedi all&#39;utente:
> Quale file o cartella desideri arricchire?
> - File singolo: percorso relativo alla directory principale dell&#39;archivio (ad esempio `help/using/email/get-started-email.md`)
> - Cartella: tutti i `.md` file in modo ricorsivo (esempio: `help/using/email`)
> - Elenco di file/cartelle

Se viene specificata una cartella, elencare i file `.md` trovati e confermare prima dell&#39;elaborazione.

### Passaggio 2 — Per ogni file: leggere e generare

1. **Leggi il file** per intero.
2. **Comprendere l&#39;argomento della pagina**: quale funzione, concetto o attività copre?
3. **Generare il contenuto del blocco** utilizzando le regole di generazione del contenuto seguenti.
4. **Esegui l&#39;elenco di controllo della convalida di post-generazione** (vedi sotto) — non saltare.
5. **Verificare** se esiste già un blocco di riferimento della Knowledge Base, in linea (`+++ AI Knowledge Reference` vicino alla fine) o già esternalizzato (una riga `{{$include /help/_includes/do-not-localize/.../ai-augmented-...}}`). In caso affermativo, chiedere all’utente: sostituire o saltare? Al momento della sostituzione, sovrascrivi il file di inclusione (e se il blocco era ancora in linea, rimuovi il blocco in linea e aggiungi invece la riga di inclusione).

### Passaggio 3: verificare tutte le richieste di risarcimento nei confronti del corpo della pagina

Prima di scrivere il blocco, rileggere l&#39;attestazione di contenuto generato per attestazione. Questo passaggio è **obbligatorio e non può essere saltato**, anche per i file brevi. Correggere eventuali errori prima di procedere al punto 4.

**Terminologia ed etichette**

- [ ] Ogni termine, etichetta e nome dell&#39;interfaccia utente nel blocco viene visualizzato nel corpo della pagina, non viene importato da un&#39;altra pagina o dedotto dalla conoscenza generale del prodotto
- [ ] Non viene elencato alcun sinonimo a meno che entrambi i moduli non vengano visualizzati nella pagina
- [ ] Ogni voce &quot;Non confondere&quot; fa riferimento solo ai concetti menzionati in questa pagina

**Guardrail e limiti**

- [ ] Ogni valore numerico corrisponde esattamente al corpo della pagina
- [ ] Un limite viene chiamato **rigido** solo se il corpo della pagina utilizza tale parola o implica chiaramente che il sistema lo applica (ad esempio, &quot;non può superare&quot;, &quot;massimo ... consentito&quot;, &quot;solo ... supportato&quot;)
- [ ] Un limite è chiamato **consigliato** solo se il corpo della pagina utilizza quella parola o un equivalente (&quot;per prestazioni migliori&quot;, &quot;è consigliato&quot;)
- [ ] Se il corpo della pagina non fornisce qualificatori, il blocco non fornisce alcun qualificatore. Non crearne uno
- [ ] Nessun meta-commento su ciò che la pagina sorgente dice o meno (ad esempio, &quot;nessun numero specifico è indicato in questa pagina&quot;)

**Definizioni glossario**

- [ ] Nessuna definizione contiene dettagli tecnici assenti dal corpo della pagina
- [ ] Nessuna voce viene elaborata utilizzando informazioni provenienti da altre pagine del set di documentazione

**Risposte alle domande frequenti**

- [ ] Ogni dettaglio specifico (costi dell&#39;interfaccia utente, nomi di pulsanti, nomi di campi, sequenze di passaggi) è indicato nel corpo della pagina, non dedotto né importato da altre pagine
- [ ] Nessuna risposta introduce informazioni alle quali il corpo della pagina non si rivolge

**Regola di correzione:** Se un controllo non riesce, correggere il contenuto **prima** della scrittura del blocco. Registra ogni correzione nel rapporto del passaggio 5.

&#x200B;---

### Passaggio 4: scrivere il blocco in un&#39;inclusione do-not-localize, quindi includerlo

Il blocco generato non deve essere **localizzato**, pertanto non viene scritto in linea nella pagina. Risiede invece in un file di inclusione separato in `help/_includes/do-not-localize/`, che viene escluso dalla traduzione, e la pagina lo richiama con `{{$include}}`. Questa è la convenzione DOCAC-15581.

**a. Derivare il nome del file di inclusione** dal percorso della pagina relativo alla cartella della sezione di livello superiore in `help/using/`: rimuovere l&#39;estensione `.md`, sostituire eventuali `/` rimanenti con `-` e aggiungere il prefisso `ai-augmented-`. Questo appiattimento consente di mantenere la directory piatta priva di collisioni.

Esempi (sezione `building-journeys`):

| Pagina | Includi file |
|---|---|
| `help/using/building-journeys/end-journey.md` | `ai-augmented-end-journey.md` |
| `help/using/building-journeys/expression/journey-properties.md` | `ai-augmented-expression-journey-properties.md` |

**b. Scrivere il file di inclusione** in `help/_includes/do-not-localize/<section-folder>/<include-file>` (creare la sottodirectory `<section-folder>` se non esiste, una sottocartella per sezione AJO di livello principale, ad esempio `building-journeys/`, `email/`). Utilizza esattamente questa struttura: `title` frontmatter, un&#39;intestazione `# AI Knowledge Reference`, il pannello a soffietto completo dal **modello completo** di seguito, quindi il commento di sincronizzazione:

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

[complete "+++ AI Knowledge Reference" accordion from the Full template below]

<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of the including page's body, excluding the {{$include}} line] -->
```

**c. Aggiungere la chiamata di inclusione** come ultima riga della pagina, preceduta da una riga vuota. Non modificare altri contenuti della pagina:

```
{{$include /help/_includes/do-not-localize/<section-folder>/<include-file>}}
```

Il commento di sincronizzazione consente ancora il rilevamento della deriva: l’hash di origine viene calcolato sul corpo della pagina inclusa, in modo che in futuro gli strumenti e gli autori possano capire quando la pagina si è spostata dal blocco. Due file cambiano per pagina: il **file di inclusione** (creato) e la **pagina** (aggiunta una `{{$include}}` riga).

### Passaggio 5 — Rapporto

- File modificati ✓ (includere il file creato + la riga `{{$include}}` della pagina)
- File ignorati + motivo (ha già una pagina di blocco / vuota / indice)
- Eventuali avvisi di convalida generati durante il passaggio 2

&#x200B;---

## Regole di generazione dei contenuti

Analizza la pagina e genera le sezioni seguenti **in ordine** all&#39;interno del pannello a soffietto. Ignora completamente una sezione se non è possibile estrarre contenuto significativo.

### Apertura fissa - non modificare

Ogni pannello a soffietto di riferimento della conoscenza di IA deve iniziare con questo blocco esatto. Copiatelo così com’è; non parafrasate, condensate o riordinate:

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

Le sezioni specifiche della pagina seguenti seguono immediatamente dopo questi due paragrafi, sempre all’interno dello stesso pannello a soffietto. L’intero pannello a soffietto viene scritto nel file do-not-localize include, in base al passaggio 4, non in linea nella pagina.

### 1. TL;DR

Una frase: cosa insegna o permette questa pagina?

```
* **TL;DR:** [one sentence]
```

### &#x200B;2. Intenti

3-6 operazioni che un utente può eseguire dopo aver letto questa pagina.

```
**Intents:**

* [action]
* [action]
```

### &#x200B;3. Glossario

Termini chiave specifici di questa pagina/funzione con definizioni brevi. Contrassegna i termini specifici del prodotto.

```
**Glossary:**

* **[Term]**: [definition] *(product-specific)*
```

Includi solo i termini rilevanti per questa pagina. Non aggiungere termini di marketing generici.

**Regola di precisione modalità di convalida — obbligatoria:**
Se la pagina include qualsiasi forma di test, anteprima o esecuzione simulata, DEVI distinguere tra tutte le modalità effettivamente descritte nella pagina. Non comprimere modalità distinte in un&#39;unica voce a sintassi abbreviata:
- **Simulazione** — esegue il rendering del contenuto del messaggio senza inviare; utilizza profili reali
- **Modalità test** - invia solo ai profili di test designati; utilizza i profili di test AEP persistenti (non i profili sintetici o falsi)
- **Esecuzione in prova**: esegue la logica di percorso completa senza attivare azioni; utilizza dati di pubblico reali

Includi solo le modalità presenti nella pagina. Copiare il termine accurato del prodotto dal corpo della pagina: non sostituire &quot;profili sintetici&quot;, &quot;dati falsi&quot; o &quot;senza dati reali&quot; per nessuno di questi.

### &#x200B;4. Guardrail

Limitazioni, prerequisiti, autorizzazioni o vincoli menzionati nella pagina.

```
**Guardrails:**

* [guardrail]
```

**Regole di precisione guardrail - obbligatorie:**

- **Qualifica ogni limite numerico** come consigliato o rigido. Esempio: &quot;Massimo 10 ricerche di set di dati per messaggio (limite rigido)&quot; non &quot;Massimo 10 ricerche di set di dati&quot;.
- **Qualifica ogni velocità effettiva o valore di velocità** con il relativo ambito. Esempio: &quot;TPS cap 150.000 messaggi/ora (per sandbox)&quot; non &quot;150.000 messaggi/ora cap&quot;.
- **Verifica ogni guardrail rispetto al corpo della pagina** prima di includerlo. Se la pagina riporta 10 e il blocco indica 5, il blocco è errato. Il corpo della pagina è autorevole.
- **Non dedurre guardrail** non indicati nella pagina. Se esiste un vincolo ma la pagina non lo indica, omettilo.

### &#x200B;5. Terminologia

Nomi canonici, acronimi, varianti accettate, sinonimi, disambiguazione. Principalmente per la normalizzazione della pipeline di intelligenza artificiale.

```
**Terminology:**

* Canonical name: [name] — Acronym: [acronym] — variants: [list]
* Synonyms: "[term A]" = "[term B]"
* Do not confuse: "[term]" ≠ "[other term]"
```

**Regola di precisione stato e ciclo di vita:**
Quando la pagina descrive un ciclo di vita (stati percorso, stati messaggio, stati campagna, ecc.), copia le etichette di stato esatte dal corpo della pagina. Non parafrasare. Utilizza le voci &quot;Do not confuse&quot; per non ambiguare gli stati che condividono una parola root ma hanno un significato distinto. Esempio:

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. Domande frequenti

3-6 domande che un utente potrebbe porre, con risposte brevi.

```
**FAQ:**

* **Q: [question]** — [short answer]
```

**Regola di precisione domande frequenti:**
Le risposte devono utilizzare le stesse scelte di verbi e sostantivi del corpo della pagina. Non introdurre verbi come &quot;ripristina&quot;, &quot;ripristina&quot; o &quot;ripristina indietro&quot; a meno che la pagina non li utilizzi. Se una transizione termina una sessione (ad esempio, se esci dalla modalità di test, il percorso ritorna allo stato precedente), dica esattamente questo — non dica &quot;il percorso ritorna allo stato Bozza&quot;.

### Cosa NON includere

- **non** riscrivere o riepilogare il contenuto del corpo (è già nella pagina)
- **non** includere istruzioni dettagliate
- **not** inventa contenuto non supportato dalla pagina
- **not** utilizza i seguenti termini imprecisi a meno che non vengano visualizzati letteralmente nel corpo della pagina: &quot;sintetico&quot;, &quot;dati falsi&quot;, &quot;senza dati reali&quot;, &quot;ripristina&quot;, &quot;ripristina&quot; (quando descrivi le transizioni dello stato del prodotto)

&#x200B;---

## Elenco di controllo per la convalida post-generazione

Esegui questo elenco di controllo su ogni blocco prima di scrivere l’inclusione. Segnala eventuali errori all’utente prima di procedere.

### Controllo guardrail

- [ ] Ogni valore numerico nel blocco esiste letteralmente o è derivabile dal corpo della pagina
- [ ] Ogni limite è qualificato come consigliato o rigido
- [ ] Ogni figura di velocità effettiva include il relativo ambito (sandbox/organizzazione/istanza)

### Verifica terminologica
- [ ] Tutte le modalità di convalida (simulazione, modalità di test, esecuzione in prova) presenti nella pagina sono incluse e denominate con termini accurati nella pagina
- [ ] Tutti gli stati del ciclo di vita utilizzano le etichette esatte del corpo della pagina
- [ ] Nessun verbo impreciso nelle risposte alle domande frequenti (&quot;ripristina&quot;, &quot;sintetico&quot;, &quot;dati falsi&quot;, &quot;senza dati reali&quot;) a meno che non sia presente il testo nella pagina

### Verifica ambito
- [ Il glossario ] non contiene termini di marketing generici non correlati alla pagina
- [ ] Le risposte alle domande frequenti non introducono informazioni assenti dalla pagina

Se una verifica non riesce, correggi il blocco prima di scrivere l’inclusione. Registra la correzione nel rapporto del passaggio 5.

&#x200B;---

## Responsabilità di sincronizzazione

Il blocco di riferimento della conoscenza AI è una derivata del corpo della pagina in un determinato momento. Deve essere trattata come parte della pagina.

**Quando il corpo della pagina viene aggiornato (PR della versione, correzioni, ecc.):**

- Se l’aggiornamento modifica un guardrail, un limite, un’etichetta di stato o una modalità di convalida descritti nel blocco, → rigenerare o aggiornare manualmente il blocco nella stessa PR.
- Se l’aggiornamento non è correlato al contenuto del blocco (ad esempio passaggi della procedura, aggiornamenti della schermata) → il blocco può rimanere invariato, ma rivederlo brevemente.

Il commento di sincronizzazione all&#39;interno del file di inclusione (`<!-- ai-section-version -->`) è il segnale: se il corpo della pagina di inclusione è cambiato da quando è stato scritto l&#39;hash, il blocco è un candidato per la revisione. Durante l&#39;aggiornamento, modificare il file di inclusione in `help/_includes/do-not-localize/`, non la pagina.

&#x200B;---

## Modello completo

File di inclusione (`help/_includes/do-not-localize/<section-folder>/ai-augmented-<page>.md`):

```markdown
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

* **TL;DR:** [one sentence]

**Intents:**

* [intent]

**Glossary:**

* **[Term]**: [definition] *(product-specific)*

**Guardrails:**

* [guardrail — qualify each numeric limit as recommended|hard, each throughput figure with scope sandbox|org]

**Terminology:**

* Canonical name: [name] — Acronym: [acronym] — variants: [variants]
* Synonyms: "[a]" = "[b]"
* Do not confuse: "[x]" ≠ "[y]"

**FAQ:**

* **Q: [question]** — [short answer]

+++

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

Riga aggiunta alla pagina:

```
{{$include /help/_includes/do-not-localize/building-journeys/ai-augmented-end-journey.md}}
```

## Note

- Elabora i file uno per uno per qualità.
- Contrassegna le pagine molto brevi o solo indice e chiedi all’utente se saltare.
- L&#39;unico nuovo file creato per pagina è do-not-localize include (Passaggio 4); la pagina stessa viene modificata solo per aggiungere la singola riga `{{$include}}`. In caso contrario, non creare o ristrutturare i file.
- L’elenco di controllo della convalida di post-generazione non è facoltativo. Eseguirlo per ogni file, comprese le operazioni in blocco.
