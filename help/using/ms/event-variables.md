---
solution: Journey Optimizer
product: journey optimizer
title: Variabili evento campagna con più passaggi
description: Scopri come sfruttare le variabili evento nelle campagne con più passaggi
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---

# Variabili evento campagna con più passaggi {#event-variables}

Alcune attività di campagna in più passaggi consentono di modificare gli script nell’editor di espressioni per eseguire azioni specifiche, ad esempio recuperare dati provenienti da attività precedenti, creare condizioni o calcolare nomi di file in base a variabili evento.

## Cosa sono le variabili evento {#scripting}

Gli script eseguiti nel contesto di una campagna con più passaggi accedono a una serie di **oggetti** globali aggiuntivi, ad esempio la campagna con più passaggi in esecuzione (`ìnstance`), le varie attività (`task`) o gli eventi che hanno attivato una determinata attività (`event`).

A ogni tipo di **oggetto** è associata una categoria di **variabili** che possono essere utilizzate nell&#39;editor espressioni durante la modifica di script in attività quali **[!UICONTROL codice JavaScript]** o **[!UICONTROL Test]**.

* **Le variabili di istanza** (`instance.vars.xxx`) sono paragonabili alle variabili globali. Sono condivise da tutte le attività.
* **Le variabili attività** (`task.vars.xxx`) sono paragonabili alle variabili locali. Vengono utilizzati solo dall&#39;attività corrente. Queste variabili vengono utilizzate dalle attività persistenti per conservare i dati e talvolta vengono utilizzate per scambiare dati tra i diversi script di una stessa attività.
* **Le variabili evento** (`vars.xxx`) consentono lo scambio di dati tra le attività elementari di un processo di campagna in più passaggi. Queste variabili vengono passate dall&#39;attività che ha attivato l&#39;attività in corso. Vengono quindi passate alle seguenti attività. **Le variabili evento** sono le variabili utilizzate più di frequente e devono essere utilizzate al posto delle variabili di istanza.

## Sfruttare le variabili di evento nell’editor di espressioni {#expression-editor}

Le variabili di evento predefinite sono disponibili per l’utilizzo nel riquadro a sinistra dell’editor di espressioni. Puoi anche crearne di nuovi inizializzando una nuova variabile nel codice.

![](assets/event-variables.png)

Oltre a queste variabili evento, puoi anche sfruttare il menu **[!UICONTROL Condizioni]** nel riquadro a sinistra per creare le condizioni e il menu **[!UICONTROL Aggiungi data corrente]** per utilizzare le funzioni relative alla formattazione delle date.
