---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 4%

---
# Specifica di generazione: blocchi di riferimento della conoscenza IA

L’unica fonte di verità per ciò che contiene un blocco di riferimento della conoscenza basata sull’intelligenza artificiale e come è
scritto. Seguilo esattamente per ogni pagina. (che rispecchia la
`.claude/commands/augmentedAIContent.md`; l&#39;abilità è la versione canonica.)

## Regola d&#39;oro

Un blocco può contenere **solo ciò che è derivabile dal proprio corpo pagina.** Non altre pagine, non
conoscenza generale del prodotto, non contenuti con commenti o commenti di HTML. Se la pagina non indica
e nemmeno il blocco.

## Pannello a soffietto + includi sintassi

```
+++ AI Knowledge Reference

Content here — standard markdown.

+++
```

- Apertura di `+++ AI Knowledge Reference` (uno spazio dopo `+++`); chiusura di `+++` da sola.
- Riga vuota prima dell&#39;apertura `+++` e dopo la chiusura `+++`.
- Il titolo è sempre esattamente `AI Knowledge Reference`.
- L’intero pannello a soffietto vive in un’inclusione do-not-localize e la pagina la richiama con
  `{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}`. Contenuto in
  `help/_includes/do-not-localize/` è escluso dalla localizzazione — questo è il modo in cui il blocco rimane
  non tradotto.

## Includi struttura file

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening — verbatim]

[the six sections in order]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of page body> -->
```

- **Nome file:** deriva dal percorso della pagina relativo al suo livello principale `help/using/<folder>/`
sezione: strip `.md`, sostituire i `/` rimanenti con `-`, prefisso con `ai-augmented-`.
  - `help/using/building-journeys/end-journey.md` → `ai-augmented-end-journey.md`
  - `help/using/building-journeys/expression/journey-properties.md` →
    `ai-augmented-expression-journey-properties.md`
- Una sottocartella per sezione di primo livello (`building-journeys/`, `email/`, `data/`, ...).

## Apertura fissa - testo integrale, mai modificare

Ogni blocco inizia esattamente con questi due paragrafi. Copia byte per byte; non parafrasare,
condensa o riordina:

```
This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

## Le sei sezioni, in ordine

Ignora una sezione solo se la pagina non produce alcun contenuto significativo.

### 1. TL;DR
Una frase: ciò che la pagina insegna o abilita. `* **TL;DR:** [one sentence]`

### &#x200B;2. Intenti
3-6 operazioni che un utente può eseguire dopo aver letto la pagina.

### &#x200B;3. Glossario
Termini chiave specifici della pagina con definizioni brevi; contrassegna termini specifici del prodotto con
`*(product-specific)*`. Nessuna spaziatura interna di marketing generica.

**Precisione modalità di convalida (obbligatoria):** se la pagina include test/anteprima/simulazioni
esecuzione, distingui ogni modalità effettivamente nominata dalla pagina, non comprimerle. Utilizza i
termine esatto della pagina (ad esempio `Simulate content`, `Simulate content (AEP profiles)`,
`Send proof`, `Test mode`, `Dry run`, `Simulation`, `test profile`, `sample input`). Mai
sostituisci &quot;profili sintetici&quot;, &quot;dati falsi&quot; o &quot;senza dati reali&quot; per uno di essi.

### &#x200B;4. Guardrail
Limiti, prerequisiti, autorizzazioni, vincoli indicati nella pagina.

- **Qualifica ogni limite numerico** come `(hard limit)` o `(recommended)` — ma **solo** quando
la pagina utilizza il testo di imposizione (errore / rifiutato / massimo / non può superare / solo ... supportato)
o la formulazione di consigli (per ottenere prestazioni migliori / si consiglia). Se la pagina non fornisce
qualificatore, non dare nulla. **Non etichettare mai come rigido un valore raisable, predefinito o configurabile.**
I valori che possono essere generati &quot;contattando il rappresentante Adobe&quot; o tramite un’API sono
  `(default)`, non difficile.
- **Qualifica ogni valore di velocità effettiva/velocità con il relativo ambito** (per sandbox/per organizzazione/per istanza).
- **Verifica incrociata di ogni numero con il corpo della pagina.** Il corpo della pagina è autorevole.
- **Non dedurre** guardrail che la pagina non è in stato. Nessun meta-commento (&quot;la pagina non
specificare ...&quot;).

### &#x200B;5. Terminologia
Nomi canonici, acronimi, varianti, sinonimi, disambiguazione.

- **Sinonimi** (`"A" = "B"`) solo per **equivalenti veri**. Entrambi i moduli devono essere visualizzati nella pagina
significa la stessa cosa. Tutto ciò che è un *contrasto* va sotto **Non confondere**
(`"X" ≠ "Y"`), non Sinonimi.
- **Precisione stato/ciclo di vita:** copiare le etichette di stato esatte dal corpo della pagina; non copiarle
parafrasi. Utilizzare &quot;Non confondere&quot; per separare gli stati che condividono una parola root.

### &#x200B;6. Domande frequenti
3-6 domande con risposte brevi. Le risposte utilizzano **gli stessi verbi e sostantivi della pagina
corpo**. Non introdurre &quot;ripristina&quot;, &quot;ripristina&quot; o &quot;ripristina indietro&quot; a meno che la pagina non li utilizzi.

## Cosa NON includere

- Non riscrivere o riepilogare il contenuto del corpo e non fornire istruzioni dettagliate.
- Non creare contenuti non supportati dalla pagina.
- Non utilizzare questi termini imprecisi a meno che non vengano visualizzati **letteralmente** nella pagina:
&quot;sintetico&quot;, &quot;dati falsi&quot;, &quot;senza dati reali&quot;, &quot;ripristina&quot;, &quot;ripristina&quot;.
- **Nessuna contrazione** in qualsiasi punto della prosa a blocchi — scrivi &quot;non è&quot;, &quot;non è&quot;, &quot;non può&quot;,
&quot;it is&quot;, ecc. (L’unica eccezione è una stringa dell’interfaccia utente del prodotto letterale come
  `[!UICONTROL configuration doesn't exist]`, che è conservato esattamente.)

## Passaggio 3 — verificare ogni richiesta (autocontrollo, gate 1)

Prima di scrivere l&#39;inclusione, rileggere l&#39;attestazione di contenuto generato per attestazione. Obbligatorio, anche per
pagine brevi. Correggi eventuali errori prima di scriverli e registra la correzione nel report.

- Ogni termine/etichetta/nome interfaccia utente nel blocco viene visualizzato nel corpo della pagina.
- Nessun sinonimo a meno che entrambi i moduli non vengano visualizzati nella pagina; ogni riferimento &quot;Non confondere&quot; è riservato
concetti in questa pagina.
- Ogni valore numerico corrisponde esattamente al corpo della pagina; ogni qualificatore di limite è giustificato dal
testo della pagina; nessun qualificatore inventato.
- Nessun glossario/domanda frequente importato da altre pagine o informazioni generali.
- Nessun termine impreciso vietato a meno che non sia riportato sulla pagina, nessuna contrazione.

## Lista di controllo post-generazione (gate 1, continua)

- [ ] Ogni valore numerico esiste letteralmente / è derivabile dal corpo della pagina.
- [ ] Ogni limite è stato qualificato correttamente (hard vs. consigliato vs. nessuno); nessun valore predefinito/stimabile
 erroneamente etichettato come duro.
- [ ] Ogni figura di velocità effettiva ha il proprio ambito.
- [ ] Tutte le modalità di convalida presenti nella pagina sono denominate con termini accurati.
- [ ] Tutti gli stati del ciclo di vita utilizzano etichette di pagina esatte.
- [ ] I sinonimi sono veri equivalenti; i contrasti sono in &quot;Non confondere&quot;.
- [ ] Nessuna parola vietata / nessuna contrazione (al di fuori delle stringhe letterali dell&#39;interfaccia utente).
- [ Il glossario di ] non contiene termini generici; nelle domande frequenti non viene introdotto nulla che non sia presente nella pagina.

Gate 1 è l&#39;autore del blocco che controlla il proprio lavoro. **not** sostituisce il
verifica indipendente (gate 2) in `verification-round.md`.
