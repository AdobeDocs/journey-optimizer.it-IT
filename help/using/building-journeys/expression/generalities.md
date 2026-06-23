---
solution: Journey Optimizer
product: journey optimizer
title: Sintassi dell’editor espressioni avanzato
description: Scopri la sintassi utilizzata nell’editor di espressioni avanzate
feature: Journeys
role: Developer
level: Experienced
keywords: sintassi, editor, percorso
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/-PTYUf-njT3-LsI-A5IKEMDGOl4JecZ-ayM0rU4f2HI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 620
ht-degree: 2%

---

# Sintassi dell’editor espressioni avanzato {#syntax}

Le informazioni di base sulla sintassi quando si utilizza l&#39;[Editor di espressioni avanzate](expressionadvanced.md) sono elencate di seguito. <!-- Samples of use of the advanced expression editor are available on [this page](advanced-editor-use-cases.md).-->

## Priorità tra parentesi ed espressione {#parentheses-and-expression-priority}

Le parentesi possono essere utilizzate per rendere più leggibile un&#39;espressione complessa. _(&lt;espressione>)_ equivale a _&lt;espressione>_. Le parentesi possono essere utilizzate anche per definire l&#39;ordine di valutazione e l&#39;associatività.

Le espressioni verranno valutate da sinistra a destra. L&#39;associatività sugli operatori aritmetici deve essere applicata: le moltiplicazioni e le divisioni hanno priorità rispetto alle addizioni e alle sottrazioni. Per imporre un ordine specifico, è necessario aggiungere una parentesi per delimitare le operazioni. Ad esempio:

<!--```5 + 2 * 10 = 25, and (5 + 2) * 10 = 70```-->

| Espressione | Valutazione |
|--- |--- |
| `4 + 2 * 10` | <ul><li>&#39;*&#39; ha priorità su &#39;+&#39;: 2 \* 10 viene valutato → 20</li><li>4 + 20 → 24</li></ul> |
| `(4 + 2) * 10` | <ul><li>Le parentesi modificano la priorità: (4 + 2) viene valutato → 6</li><li> 6 * 10 → 60</li></ul> |

## Distinzione tra maiuscole e minuscole {#case-sensitivity}

Di seguito sono riportate le diverse regole per la distinzione tra maiuscole e minuscole:

* Tutti gli operatori (e, o, ecc.) devono essere scritte in minuscolo. Ad esempio, _`<expression1>`e`<expression2>`_ sono espressioni valide, mentre l&#39;espressione _`<expression1>`AND`<expression2>`_ non lo è.
* Tutti i nomi di funzione fanno distinzione tra maiuscole e minuscole. Ad esempio, _inAudience()_ è valido, mentre la funzione _INAUDIENCE()_ non lo è.
* I riferimenti ai campi e i valori costanti fanno distinzione tra maiuscole e minuscole: non sono elementi incorporati del linguaggio (al contrario di operatori e funzioni), ma vengono creati dall’utente finale.

## Tipo di espressione restituito {#returned-expression-type}

A seconda del contesto di utilizzo, l’editor di espressioni può restituire valori diversi.

| Utilizzo avanzato dell’editor di espressioni | Tipo di espressione restituito previsto |
|--- |--- |
| Condizione (condizione origine dati, condizione data) | booleano |
| Timer personalizzato | dateTimeOnly |
| Mappatura dei parametri delle azioni | Any |

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina vengono illustrate le regole di sintassi di base dell&#39;editor di espressioni avanzate di Percorso, ovvero la precedenza degli operatori con parentesi, la distinzione tra maiuscole e minuscole per gli operatori e le funzioni e il tipo restituito previsto per ogni contesto dell&#39;editor.

**Intenti:**

* Controlla l’ordine di valutazione delle espressioni racchiudendo le sottoespressioni tra parentesi
* Scrittura degli operatori (`and`, `or`, `not`) in minuscolo per evitare errori di sintassi
* Utilizza nomi di funzione con maiuscole/minuscole corretti (esempio: `inAudience()` non `INAUDIENCE()`)
* Le condizioni devono restituire un valore booleano, i timer personalizzati devono restituire `dateTimeOnly` e le mappature dei parametri di azione possono restituire qualsiasi tipo

**Glossario:**

* **Priorità espressione**: ordine di valutazione degli operatori; le moltiplicazioni e le divisioni hanno priorità rispetto alle aggiunte e alle sottrazioni *(specifico per prodotto)*
* **Distinzione maiuscole/minuscole**: nell&#39;editor avanzato, gli operatori devono essere minuscole, i nomi delle funzioni devono fare distinzione tra maiuscole e minuscole e i riferimenti ai campi devono fare distinzione tra maiuscole e minuscole in base a quanto creato dall&#39;utente *(specifico per prodotto)*
* **dateTimeOnly**: il tipo restituito richiesto per le espressioni timer personalizzate (attività di attesa); rappresenta una data/ora senza un fuso orario *(specifico per prodotto)*

**Guardrail:**

* Operatori (`and`, `or`, `not`, ecc.) deve essere scritto in minuscolo; le varianti maiuscole non sono valide
* Tutti i nomi di funzione fanno distinzione tra maiuscole e minuscole. `inAudience()` è valido ma `INAUDIENCE()` non lo è
* L&#39;aritmetica segue la precedenza standard: `*` e `/` valutano prima di `+` e `-`; utilizzare le parentesi per ignorare
* Le condizioni restituiscono sempre un valore booleano; i timer personalizzati restituiscono sempre `dateTimeOnly`

**Terminologia:**

* Nome canonico: Advanced Expression Editor Syntax — Acronimo: none — varianti: sintassi espressione, sintassi editor
* Sinonimi: &quot;priorità espressione&quot; = &quot;precedenza operatore&quot;; &quot;parentesi&quot; = &quot;parentesi quadre&quot; (nel contesto espressione)
* Non confondere: distinzione tra maiuscole e minuscole dell&#39;operatore (gli operatori devono usare lettere minuscole) ≠ distinzione tra maiuscole e minuscole del riferimento del campo (i nomi dei campi sono scritti dall&#39;utente e con distinzione tra maiuscole e minuscole)

**Domande frequenti:**

* **Q: `4 + 2 * 10` restituisce 60 o 24?** — Restituisce 24 perché `*` ha priorità rispetto a `+`; utilizzare `(4 + 2) * 10` per ottenere 60.
* **Q: è possibile scrivere `AND` in maiuscolo in un&#39;espressione?** — No; tutti gli operatori devono essere minuscoli (`and`, `or`, `not`).
* **Q: i nomi delle funzioni sono sensibili a maiuscole e minuscole?** — Sì; `inAudience()` è valido ma `INAUDIENCE()` non lo è.
* **D: che tipo deve restituire un&#39;espressione di condizione?** — Valore booleano.
* **Q: quale tipo restituito è necessario per un&#39;espressione timer attività di attesa personalizzata?** — `dateTimeOnly`.

+++
