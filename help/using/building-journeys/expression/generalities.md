---
solution: Journey Optimizer
product: journey optimizer
title: Sintassi dell’editor espressioni avanzato
description: Scopri la sintassi utilizzata nell’editor di espressioni avanzate
feature: Journeys
role: Engineer
level: Experienced
keywords: sintassi, editor, percorso
exl-id: c9434b28-2750-4a53-985e-c4a3f940472c
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 5%

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

* Tutti gli operatori (e, o, ecc.) devono essere scritti in minuscolo. Ad esempio, _`<expression1>`e`<expression2>`_ sono espressioni valide, mentre l&#39;espressione _`<expression1>`AND`<expression2>`_ non lo è.
* Tutti i nomi di funzione fanno distinzione tra maiuscole e minuscole. Ad esempio, _inAudience()_ è valido, mentre la funzione _INAUDIENCE()_ non lo è.
* I riferimenti ai campi e i valori costanti fanno distinzione tra maiuscole e minuscole: non sono elementi incorporati del linguaggio (al contrario di operatori e funzioni), ma vengono creati dall’utente finale.

## Tipo di espressione restituito {#returned-expression-type}

A seconda del contesto di utilizzo, l’editor di espressioni può restituire valori diversi.

| Utilizzo avanzato dell’editor di espressioni | Tipo di espressione restituito previsto |
|--- |--- |
| Condizione (condizione origine dati, condizione data) | booleano |
| Timer personalizzato | dateTimeOnly |
| Mappatura dei parametri delle azioni | Qualsiasi |
