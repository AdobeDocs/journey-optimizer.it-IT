---
name: ajo-ai-accordion
description: Arricchisce le pagine della documentazione di Adobe Journey Optimizer con una sezione del Pannello a soffietto dell’Assistente di intelligenza artificiale aggiunta alla fine di ciascun file Markdown. Legge ogni pagina, genera automaticamente il contenuto rilevante dell’Assistente AI in base all’argomento della pagina e lo inserisce come pannello a soffietto comprimibile. Da utilizzare quando l’utente desidera aggiungere informazioni sull’intelligenza artificiale ai documenti di AJO, arricchire le pagine Markdown di AJO con contenuti basati sull’intelligenza artificiale oppure elaborare un file o una cartella di file Markdown con sezioni del Pannello a soffietto basate sull’intelligenza artificiale.
disable-model-invocation: true
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---


# Arricchimento del pannello a soffietto di IA per AJO

Aggiunge un pannello a soffietto dell’Assistente IA generato automaticamente alla fine di uno o più file markdown nell’archivio della documentazione di Journey Optimizer.

## Archivio di destinazione

`/Users/sauviat/GitHub/GHEC/journey-optimizer.en/help/using/`

## Sintassi Accordion (Experience League)

```markdown
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**Regole:**
- `+++Title` su una riga — il titolo segue immediatamente `+++`, nessuno spazio tra
- `+++` da solo su una riga chiude il pannello a soffietto
- Riga vuota prima dell&#39;apertura `+++` e dopo la chiusura `+++`

&#x200B;---

## Flusso di lavoro

### Passaggio 1 — Richiedi target

Chiedi all&#39;utente:

> Quale file o cartella desideri arricchire?
> - File singolo: percorso relativo alla directory principale dell&#39;archivio (ad esempio `help/using/email/get-started-email.md`)
> - Cartella: elabora tutti i `.md` file in modo ricorsivo (esempio: `help/using/email`)
> - Elenco di file/cartelle

Usa `AskQuestion` se disponibile, altrimenti chiedi a conversationally.

Se viene specificata una cartella, elencare tutti i file `.md` trovati e confermare con l&#39;utente prima dell&#39;elaborazione.

### Passaggio 2 — Per ogni file: leggere e generare

Per ogni file di destinazione:

1. **Leggi il file** per intero.
2. **Comprendere l&#39;argomento della pagina**: quale funzione, concetto o attività copre?
3. **Genera il contenuto del Pannello a soffietto** utilizzando le regole di generazione del contenuto seguenti.
4. **Verificare** se alla fine del file esiste già un pannello a soffietto di IA (cercare `+++` vicino alla fine). In caso affermativo, chiedere all&#39;utente se sostituire o saltare.

### Passaggio 3 — Aggiungere il pannello a soffietto

Aggiungi alla fine del file:

```markdown
+++[ACCORDION_TITLE]

[GENERATED_CONTENT]

+++
```

Nessun altro contenuto del file deve essere modificato.

### Passaggio 4 — Rapporto

Dopo l’elaborazione di tutti i file:
- File elenco modificati ✓
- Elenca i file ignorati e il motivo (dispone già di pannello a soffietto, file vuoto, non pertinente, ecc.)

&#x200B;---

## Regole di generazione dei contenuti

Genera il contenuto del Pannello a soffietto analizzando la pagina markdown. Produrre le seguenti sezioni **in ordine**, formattate come elenchi puntati di markdown. Ignora qualsiasi sezione per la quale non è possibile estrarre contenuto significativo dalla pagina.

&#x200B;---

### Titolo Accordion

Usa: `+++AI Assistant — Page context`

&#x200B;---

### Sezioni da generare (in ordine)

**1. TL;DR**

Una frase. Cosa insegna o abilita questa pagina?

```markdown
- **TL;DR:** [one sentence summary]
```

&#x200B;---

**2. Intenti**

Elenco puntato delle operazioni che un utente può eseguire dopo aver letto questa pagina (3-6 elementi).

```markdown
**Intents:**
- [action the user can perform]
- [action the user can perform]
```

&#x200B;---

**3. Glossario**

Termini chiave specifici di questa pagina/funzione, con una breve definizione. Contrassegna i termini specifici del prodotto.

```markdown
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
- **[Term]**: [definition]
```

Includi solo i termini rilevanti per l’argomento di questa pagina. Non aggiungere termini di marketing generici.

&#x200B;---

**4. Guardrail**

Limitazioni, prerequisiti, autorizzazioni o vincoli menzionati nella pagina.

```markdown
**Guardrails:**
- [guardrail or prerequisite]
- [guardrail or prerequisite]
```

&#x200B;---

**5. Terminologia**

Nomi di prodotti canonici, acronimi, varianti accettate, sinonimi e hint di disambiguazione. Questa sezione è principalmente per la normalizzazione della pipeline di intelligenza artificiale.

```markdown
**Terminology:**
- Canonical name: [e.g. Adobe Journey Optimizer]
- Acronym: [e.g. AJO] — variants: [e.g. Journey Optimizer, A-JO]
- Synonyms: [e.g. "brand guidelines" = "brand rules", "branding standards"]
- Do not confuse: [e.g. "AI Assistant" ≠ "Adobe Sensei"]
```

Includi solo le voci presenti o implicite nella pagina.

&#x200B;---

**6. Domande frequenti**

3-6 domande che un utente potrebbe porre sul contenuto di questa pagina, con risposte brevi.

```markdown
**FAQ:**
- **Q: [question]** — [short answer]
- **Q: [question]** — [short answer]
```

&#x200B;---

### Cosa NON includere

- **non** riscrivere o riepilogare il contenuto del corpo della pagina (è già presente).
- **non** includere istruzioni dettagliate (presenti nella pagina).
- **not** inventa contenuto non supportato dalla pagina.

&#x200B;---

### Modello pannello a soffietto completo

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
- Canonical name: [name]
- Acronym: [acronym] — variants: [variants]

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

&#x200B;---

## Note

- Elabora i file uno per uno, non in blocco, per mantenere alta la qualità della generazione.
- Se la pagina è molto breve o è puramente una pagina di reindirizzamento/indice, contrassegnala e chiedi all’utente se desidera saltarla.
- Non creare nuovi file, modifica solo i file `.md` esistenti.
