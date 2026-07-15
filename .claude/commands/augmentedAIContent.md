---
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---
# augmentedAIContent

Aggiunge una sezione **Riferimento rapido** generata automaticamente alla fine di uno o più file Markdown nell&#39;archivio della documentazione di Journey Optimizer.

## Archivio di destinazione

`help/using/` (relativo alla directory principale dell&#39;archivio)

## Sintassi di sezioni e schede (Experience League)

### Intestazione sezione

```
## Quick reference {#quick-reference}
```

### Schede

```
>[!BEGINTABS]

>[!TAB Tab name]

Content here — any standard markdown is valid.

>[!TAB Another tab]

Content here.

>[!ENDTABS]
```

**Regole:**

- `>[!BEGINTABS]` e `>[!ENDTABS]` ciascuno sulla propria riga, circondato da righe vuote
- `>[!TAB Name]` sulla propria riga, seguita da una riga vuota prima del contenuto
- I nomi delle schede sono iniziali maiuscole, brevi (1-3 parole)
- Riga vuota prima di `>[!BEGINTABS]` e dopo `>[!ENDTABS]`

---

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
3. **Generare il contenuto della sezione** utilizzando le regole di generazione del contenuto seguenti.
4. **Esegui l&#39;elenco di controllo della convalida di post-generazione** (vedi sotto) — non saltare.
5. **Verificare** se alla fine esiste già una sezione di riferimento rapido (cercare `## Quick reference` vicino alla fine). In caso affermativo, chiedere all’utente: sostituire o saltare?

### Passaggio 3: verificare tutte le richieste di risarcimento nei confronti del corpo della pagina

Prima di aggiungere, rileggere l&#39;attestazione di sezione generata per attestazione. Questo passaggio è **obbligatorio e non può essere saltato**, anche per i file brevi. Correggere eventuali errori prima di procedere al punto 4.

**Terminologia ed etichette**

- [ ] Ogni termine, etichetta e nome dell&#39;interfaccia utente nella sezione viene visualizzato nel corpo della pagina, non viene importato da un&#39;altra pagina né dedotto dalla conoscenza generale del prodotto
- [ ] Non viene elencato alcun sinonimo a meno che entrambi i moduli non vengano visualizzati nella pagina
- [ ] Ogni voce &quot;Non confondere&quot; fa riferimento solo ai concetti menzionati in questa pagina

**Guardrail e limiti**

- [ ] Ogni valore numerico corrisponde esattamente al corpo della pagina
- [ ] Un limite viene chiamato **rigido** solo se il corpo della pagina utilizza tale parola o implica chiaramente che il sistema lo applica (ad esempio, &quot;non può superare&quot;, &quot;massimo ... consentito&quot;, &quot;solo ... supportato&quot;)
- [ ] Un limite è chiamato **consigliato** solo se il corpo della pagina utilizza quella parola o un equivalente (&quot;per prestazioni migliori&quot;, &quot;è consigliato&quot;)
- [ ] Se il corpo della pagina non fornisce qualificatori, la sezione non fornisce alcun qualificatore. Non inventarne uno.
- [ ] Nessun meta-commento su ciò che la pagina sorgente dice o meno (ad esempio, &quot;nessun numero specifico è indicato in questa pagina&quot;)

**Definizioni glossario**

- [ ] Nessuna definizione contiene dettagli tecnici assenti dal corpo della pagina
- [ ] Nessuna voce viene elaborata utilizzando informazioni provenienti da altre pagine del set di documentazione

**Risposte alle domande frequenti**

- [ ] Ogni dettaglio specifico (costi dell&#39;interfaccia utente, nomi di pulsanti, nomi di campi, sequenze di passaggi) è indicato nel corpo della pagina, non dedotto né importato da altre pagine
- [ ] Nessuna risposta introduce informazioni alle quali il corpo della pagina non si rivolge

**Regola di correzione:** Se un controllo non riesce, correggere il contenuto **prima** dell&#39;aggiunta. Registra ogni correzione nel rapporto del passaggio 5.

---

### Passaggio 4 — Aggiungere la sezione

Utilizza il blocco di apertura fisso e il modello completo definiti nelle **regole di generazione dei contenuti** di seguito. Aggiungi alla fine del file, seguita immediatamente dal commento di sincronizzazione:

```
<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of file content before section] -->
```

Questo commento consente ai futuri strumenti e autori di rilevare quando il corpo della pagina è stato spostato dalla sezione. Non modificare altri contenuti.

### Passaggio 5 — Rapporto

- File modificati ✓
- File ignorati + motivo (presenta già la sezione / vuota / pagina indice)
- Eventuali avvisi di convalida generati durante il passaggio 2

---

## Regole di generazione dei contenuti

Analizza la pagina e genera le schede seguenti **in ordine**. Ignora completamente una scheda se non è possibile estrarre contenuto significativo.

### Intestazione di sezione e apertura fissa - letteralmente, non modificare

Ogni sezione di riferimento rapido deve iniziare con questo blocco esatto. Copiatelo così com’è; non parafrasate, condensate o riordinate:

```
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

Il blocco `>[!BEGINTABS]` segue immediatamente dopo questi due paragrafi.

### Scheda 1 — Panoramica

Una frase di TL;DR riepilogo di ciò che la pagina insegna o abilita, seguito da 3-6 cose che un utente può eseguire dopo aver letto questa pagina.

```
>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [action]
* [action]
```

### Scheda 2 — Glossario

Termini chiave specifici di questa pagina/funzione con definizioni brevi. Contrassegna i termini specifici del prodotto.

```
>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*
```

Includi solo i termini rilevanti per questa pagina. Non aggiungere termini di marketing generici.

**Regola di precisione modalità di convalida — obbligatoria:**
Se la pagina include qualsiasi forma di test, anteprima o esecuzione simulata, DEVI distinguere tra tutte le modalità effettivamente descritte nella pagina. Non comprimere modalità distinte in un&#39;unica voce a sintassi abbreviata:
- **Simulazione** — esegue il rendering del contenuto del messaggio senza inviare; utilizza profili reali
- **Modalità test** - invia solo ai profili di test designati; utilizza i profili di test AEP persistenti (non i profili sintetici o falsi)
- **Esecuzione in prova**: esegue la logica di percorso completa senza attivare azioni; utilizza dati di pubblico reali

Includi solo le modalità presenti nella pagina. Copiare il termine accurato del prodotto dal corpo della pagina: non sostituire &quot;profili sintetici&quot;, &quot;dati falsi&quot; o &quot;senza dati reali&quot; per nessuno di questi.

### Scheda 3 — Terminologia

Nomi canonici, acronimi, varianti accettate, sinonimi, disambiguazione. Principalmente per la normalizzazione della pipeline di intelligenza artificiale.

```
>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [list]
* **Synonyms:** "[term A]" = "[term B]"
* **Do not confuse:** "[term]" ≠ "[other term]"
```

**Regola di precisione stato e ciclo di vita:**
Quando la pagina descrive un ciclo di vita (stati percorso, stati messaggio, stati campagna, ecc.), copia le etichette di stato esatte dal corpo della pagina. Non parafrasare. Utilizza le voci &quot;Do not confuse&quot; per non ambiguare gli stati che condividono una parola root ma hanno un significato distinto. Esempio:

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### Scheda 4 — Guardrail &amp; Limitazioni

Limitazioni, prerequisiti, autorizzazioni o vincoli menzionati nella pagina.

```
>[!TAB Guardrails & Limitations]

* [guardrail]
```

**Regole di precisione guardrail - obbligatorie:**

- **Qualifica ogni limite numerico** come consigliato o rigido. Esempio: &quot;Massimo 10 ricerche di set di dati per messaggio (limite rigido)&quot; non &quot;Massimo 10 ricerche di set di dati&quot;.
- **Qualifica ogni velocità effettiva o valore di velocità** con il relativo ambito. Esempio: &quot;TPS cap 150.000 messaggi/ora (per sandbox)&quot; non &quot;150.000 messaggi/ora cap&quot;.
- **Verifica ogni guardrail rispetto al corpo della pagina** prima di includerlo. Se la pagina riporta 10 e la sezione riporta 5, la sezione è errata. Il corpo della pagina è autorevole.
- **Non dedurre guardrail** non indicati nella pagina. Se esiste un vincolo ma la pagina non lo indica, omettilo.

### Scheda 5 — Domande frequenti

3-6 domande che un utente potrebbe porre, con risposte brevi. Formattare ciascuna domanda come intestazione in grassetto seguita da una risposta di paragrafo.

```
>[!TAB FAQ]

**Q: [question]**

[short answer]
```

**Regola di precisione domande frequenti:**
Le risposte devono utilizzare le stesse scelte di verbi e sostantivi del corpo della pagina. Non introdurre verbi come &quot;ripristina&quot;, &quot;ripristina&quot; o &quot;ripristina indietro&quot; a meno che la pagina non li utilizzi. Se una transizione termina una sessione (ad esempio, se esci dalla modalità di test, il percorso ritorna allo stato precedente), dica esattamente questo — non dica &quot;il percorso ritorna allo stato Bozza&quot;.

### Cosa NON includere

- **non** riscrivere o riepilogare il contenuto del corpo (è già nella pagina)
- **non** includere istruzioni dettagliate
- **not** inventa contenuto non supportato dalla pagina
- **not** utilizza i seguenti termini imprecisi a meno che non vengano visualizzati letteralmente nel corpo della pagina: &quot;sintetico&quot;, &quot;dati falsi&quot;, &quot;senza dati reali&quot;, &quot;ripristina&quot;, &quot;ripristina&quot; (quando descrivi le transizioni dello stato del prodotto)

---

## Elenco di controllo per la convalida post-generazione

Esegui questo elenco di controllo su ogni sezione prima di aggiungere. Segnala eventuali errori all’utente prima di procedere.

### Controllo guardrail

- [ ] Ogni valore numerico nella sezione esiste letteralmente o è derivabile dal corpo della pagina
- [ ] Ogni limite è qualificato come consigliato o rigido
- [ ] Ogni figura di velocità effettiva include il relativo ambito (sandbox/organizzazione/istanza)

### Verifica terminologica
- [ ] Tutte le modalità di convalida (simulazione, modalità di test, esecuzione in prova) presenti nella pagina sono incluse e denominate con termini accurati nella pagina
- [ ] Tutti gli stati del ciclo di vita utilizzano le etichette esatte del corpo della pagina
- [ ] Nessun verbo impreciso nelle risposte alle domande frequenti (&quot;ripristina&quot;, &quot;sintetico&quot;, &quot;dati falsi&quot;, &quot;senza dati reali&quot;) a meno che non sia presente il testo nella pagina

### Verifica ambito
- [ Il glossario ] non contiene termini di marketing generici non correlati alla pagina
- [ ] Le risposte alle domande frequenti non introducono informazioni assenti dalla pagina

Se un controllo non riesce, correggi la sezione prima di aggiungere. Registra la correzione nel rapporto del passaggio 4.

---

## Responsabilità di sincronizzazione

La sezione Riferimento rapido è una derivata del corpo della pagina in un determinato momento. Deve essere trattata come parte della pagina.

**Quando il corpo della pagina viene aggiornato (PR della versione, correzioni, ecc.):**

- Se l’aggiornamento modifica un guardrail, un limite, un’etichetta di stato o una modalità di convalida descritti nella sezione, → rigenerare o aggiornare manualmente la sezione nella stessa PR.
- Se l’aggiornamento non è correlato al contenuto della sezione (ad esempio passaggi della procedura, aggiornamenti delle schermate) → sezione potrebbe rimanere invariato, ma rivederlo brevemente.

Il commento di sincronizzazione aggiunto dopo la sezione (`<!-- ai-section-version -->`) è il segnale: se il contenuto del file prima della sezione è stato modificato dopo la scrittura dell&#39;hash, la sezione è un candidato per la revisione.

---

## Modello completo

```markdown
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

>[!BEGINTABS]

>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [intent]

>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*

>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [variants]
* **Synonyms:** "[a]" = "[b]"
* **Do not confuse:** "[x]" ≠ "[y]"

>[!TAB Guardrails & Limitations]

* [guardrail — type: recommended|hard — scope: sandbox|org]

>[!TAB FAQ]

**Q: [question]**

[short answer]

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

## Note

- Elabora i file uno per uno per qualità.
- Contrassegna le pagine molto brevi o solo indice e chiedi all’utente se saltare.
- Non creare nuovi file, modifica solo i file `.md` esistenti.
- L’elenco di controllo della convalida di post-generazione non è facoltativo. Eseguirlo per ogni file, comprese le operazioni in blocco.
