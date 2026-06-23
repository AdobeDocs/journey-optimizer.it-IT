---
source-git-commit: c81615909e033d52fbed56f0195467a3e346a4be
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 1%

---
# augmentedAIContent

Aggiunge un pannello a soffietto dell’Assistente IA generato automaticamente alla fine di uno o più file markdown nell’archivio della documentazione di Journey Optimizer.

## Archivio di destinazione

`help/using/` (relativo alla directory principale dell&#39;archivio)

## Sintassi Accordion (Experience League)

```
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Regole:**
- `+++Title` su una riga — il titolo segue immediatamente `+++`
- `+++` da solo su una riga chiude il pannello a soffietto
- Riga vuota prima dell&#39;apertura `+++` e dopo la chiusura `+++`

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
3. **Genera il contenuto del Pannello a soffietto** utilizzando le regole di generazione del contenuto seguenti.
4. **Esegui l&#39;elenco di controllo della convalida di post-generazione** (vedi sotto) — non saltare.
5. **Verificare** se alla fine esiste già un pannello a soffietto di IA (cercare `+++AI Knowledge Reference` vicino alla fine). In caso affermativo, chiedere all’utente: sostituire o saltare?

### Passaggio 3 — Aggiungere il pannello a soffietto

Utilizza il blocco di apertura fisso e il modello completo definiti nelle **regole di generazione dei contenuti** di seguito. Aggiungi alla fine del file, seguita immediatamente dal commento di sincronizzazione:

```
<!-- ai-accordion-version: 1 | source-hash: [first 8 chars of MD5 of file content before accordion] -->
```

Questo commento consente ai futuri strumenti e autori di rilevare quando il corpo della pagina si è allontanato dal Pannello a soffietto. Non modificare altri contenuti.

### Passaggio 4 — Rapporto

- File modificati ✓
- File ignorati + motivo (ha già il Pannello a soffietto / vuoto / pagina di indice)
- Eventuali avvisi di convalida generati durante il passaggio 2

---

## Regole di generazione dei contenuti

Analizza la pagina e genera le sezioni seguenti **in ordine** come elenchi puntati di markdown. Salta le sezioni in cui non è possibile estrarre contenuto significativo.

### Titolo pannello a soffietto e apertura fissa - non modificare

Ogni pannello a soffietto deve iniziare con questo esatto blocco. Copiatelo così com’è; non parafrasate, condensate o riordinate:

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

Le sezioni del contenuto generato seguono immediatamente questi due paragrafi.

### 1. TL;DR

Riepilogo di una frase di ciò che la pagina insegna o abilita.

```
- **TL;DR:** [one sentence]
```

### &#x200B;2. Intenti

3-6 operazioni che un utente può eseguire dopo aver letto questa pagina.

```
**Intents:**
- [action]
- [action]
```

### &#x200B;3. Glossario

Termini chiave specifici di questa pagina/funzione con definizioni brevi. Contrassegna i termini specifici del prodotto.

```
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
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
- [guardrail]
```

**Regole di precisione guardrail - obbligatorie:**

- **Qualifica ogni limite numerico** come consigliato o rigido. Esempio: &quot;Massimo 10 ricerche di set di dati per messaggio (limite rigido)&quot; non &quot;Massimo 10 ricerche di set di dati&quot;.
- **Qualifica ogni velocità effettiva o valore di velocità** con il relativo ambito. Esempio: &quot;TPS cap 150.000 messaggi/ora (per sandbox)&quot; non &quot;150.000 messaggi/ora cap&quot;.
- **Verifica ogni guardrail rispetto al corpo della pagina** prima di includerlo. Se la pagina riporta 10 e il soffietto indica 5, il soffietto è sbagliato. Il corpo della pagina è autorevole.
- **Non dedurre guardrail** non indicati nella pagina. Se esiste un vincolo ma la pagina non lo indica, omettilo.

### &#x200B;5. Terminologia

Nomi canonici, acronimi, varianti accettate, sinonimi, disambiguazione. Principalmente per la normalizzazione della pipeline di intelligenza artificiale.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

**Regola di precisione stato e ciclo di vita:**
Quando la pagina descrive un ciclo di vita (stati percorso, stati messaggio, stati campagna, ecc.), copia le etichette di stato esatte dal corpo della pagina. Non parafrasare. Utilizza le voci &quot;Do not confuse&quot; per non ambiguare gli stati che condividono una parola root ma hanno un significato distinto. Esempio:

```
- Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. Domande frequenti

3-6 domande che un utente potrebbe porre, con risposte brevi.

```
**FAQ:**
- **Q: [question]** — [short answer]
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

Esegui questo elenco di controllo su ogni pannello a soffietto prima di aggiungere. Segnala eventuali errori all’utente prima di procedere.

### Controllo guardrail
- [ ] Ogni valore numerico nel Pannello a soffietto esiste letteralmente o è derivabile dal corpo della pagina
- [ ] Ogni limite è qualificato come consigliato o rigido
- [ ] Ogni figura di velocità effettiva include il relativo ambito (sandbox/organizzazione/istanza)

### Verifica terminologica
- [ ] Tutte le modalità di convalida (simulazione, modalità di test, esecuzione in prova) presenti nella pagina sono incluse e denominate con termini accurati nella pagina
- [ ] Tutti gli stati del ciclo di vita utilizzano le etichette esatte del corpo della pagina
- [ ] Nessun verbo impreciso nelle risposte alle domande frequenti (&quot;ripristina&quot;, &quot;sintetico&quot;, &quot;dati falsi&quot;, &quot;senza dati reali&quot;) a meno che non sia presente il testo nella pagina

### Verifica ambito
- [ Il glossario ] non contiene termini di marketing generici non correlati alla pagina
- [ ] Le risposte alle domande frequenti non introducono informazioni assenti dalla pagina

Se un controllo non va a buon fine, correggi il pannello a soffietto prima di aggiungere. Registra la correzione nel rapporto del passaggio 4.

---

## Responsabilità di sincronizzazione

Il pannello a soffietto è una derivata del corpo della pagina in un determinato momento. Deve essere trattata come parte della pagina.

**Quando il corpo della pagina viene aggiornato (PR della versione, correzioni, ecc.):**
- Se l’aggiornamento modifica un guardrail, un limite, un’etichetta di stato o una modalità di convalida descritti nel Pannello a soffietto, → rigenerarlo o aggiornarlo manualmente nella stessa PR.
- Se l’aggiornamento non è correlato al contenuto del Pannello a soffietto (ad es. passaggi della procedura, aggiornamenti della schermata) → il Pannello a soffietto potrebbe rimanere invariato, ma rivederlo brevemente.

Il commento di sincronizzazione aggiunto dopo il pannello a soffietto (`<!-- ai-accordion-version -->`) è il segnale: se il contenuto del file prima del pannello a soffietto è cambiato da quando è stato scritto l&#39;hash, il pannello a soffietto è un candidato per la revisione.

---

## Modello completo

```markdown
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail — type: recommended|hard — scope: sandbox|org]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
<!-- ai-accordion-version: 1 | source-hash: [hash] -->
```

---

## Note

- Elabora i file uno per uno per qualità.
- Contrassegna le pagine molto brevi o solo indice e chiedi all’utente se saltare.
- Non creare nuovi file, modifica solo i file `.md` esistenti.
- L’elenco di controllo della convalida di post-generazione non è facoltativo. Eseguirlo per ogni file, comprese le operazioni in blocco.
