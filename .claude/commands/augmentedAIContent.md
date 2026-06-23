---
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

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
3. **Genera il contenuto del Pannello a soffietto** utilizzando le regole seguenti.
4. **Verificare** se alla fine esiste già un pannello a soffietto di IA (cercare `+++AI Assistant` vicino alla fine). In caso affermativo, chiedere all’utente: sostituire o saltare?

### Passaggio 3 — Aggiungere il pannello a soffietto

Aggiungi alla fine del file. Non modificare altri contenuti.

### Passaggio 4 — Rapporto

- File modificati ✓
- File ignorati + motivo (ha già il Pannello a soffietto / vuoto / pagina di indice)

---

## Regole di generazione dei contenuti

Analizza la pagina e genera le sezioni seguenti **in ordine** come elenchi puntati di markdown. Salta le sezioni in cui non è possibile estrarre contenuto significativo.

### Titolo Accordion

`+++AI Assistant — Page context`

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

### &#x200B;4. Guardrail

Limitazioni, prerequisiti, autorizzazioni o vincoli menzionati nella pagina.

```
**Guardrails:**
- [guardrail]
```

### &#x200B;5. Terminologia

Nomi canonici, acronimi, varianti accettate, sinonimi, disambiguazione. Principalmente per la normalizzazione della pipeline di intelligenza artificiale.

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

### &#x200B;6. Domande frequenti

3-6 domande che un utente potrebbe porre, con risposte brevi.

```
**FAQ:**
- **Q: [question]** — [short answer]
```

### Cosa NON includere

- **non** riscrivere o riepilogare il contenuto del corpo (è già nella pagina)
- **non** includere istruzioni dettagliate
- **not** inventa contenuto non supportato dalla pagina

### Modello completo

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
- [guardrail]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

---

## Note

- Elabora i file uno per uno per qualità.
- Contrassegna le pagine molto brevi o solo indice e chiedi all’utente se saltare.
- Non creare nuovi file, modifica solo i file `.md` esistenti.
