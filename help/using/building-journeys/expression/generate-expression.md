---
solution: Journey Optimizer
product: journey optimizer
title: Generare espressioni con IA
description: Scopri come utilizzare l’intelligenza artificiale in Adobe Journey Optimizer per generare espressioni direttamente nell’editor di espressioni avanzate di Percorso utilizzando prompt in linguaggio naturale.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="Beta pubblica" type="Informative"
mini-toc-levels: 2
feature_v2: []
subfeature_v2: []
source-git-commit: 423db08a3c4c5a8d9540fa0c8e03e28ca36ca299
workflow-type: tm+mt
source-wordcount: 1132
ht-degree: 2%

---


# Generare espressioni con IA {#generate-expression}

>[!CONTEXTUALHELP]
>id="journeyExpAI"
>title="Generare espressioni con IA"
>abstract="Utilizza l’intelligenza artificiale per generare e generare espressioni direttamente nell’editor di espressioni avanzate del Percorso. Ad esempio, nelle condizioni, nelle attività **Ottimizza** o nelle attività **Attendi** che utilizzano una data personalizzata. Quando descrivi ciò che ti serve in linguaggio semplice, AI genera l’espressione corrispondente."

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta pubblica**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](../../rn/releases.md).
>
>Prima di utilizzare questa funzionalità, leggi le [protezioni e limitazioni](../../content-management/gs-generative.md#generative-guardrails) correlate che si applicano alle funzioni di intelligenza artificiale generativa in Journey Optimizer.

Questa funzionalità basata sull’intelligenza artificiale, integrata nell’editor di espressioni avanzate di Percorso, consente di generare espressioni valide dai prompt di linguaggio semplice.

È disponibile ovunque si apra l&#39;editor di espressioni avanzate **del Percorso.** Ad esempio, quando configuri condizioni e routing all&#39;interno di un&#39;attività **[Ottimizza](../optimize.md)** o quando configuri un&#39;attività [**[!UICONTROL Attendi &#x200B;]**](../wait-activity.md) che utilizza una data personalizzata e hai bisogno di un&#39;espressione `dateTimeOnly`.

## Generare un’espressione {#generate}

Per generare un’espressione con IA:

1. Apri l&#39;**[!UICONTROL Editor espressioni avanzate]** nel percorso, ad esempio da una condizione di diramazione, da un&#39;attività **[!UICONTROL Ottimizza]** o da un&#39;attività **[!UICONTROL Attendi]** con una data personalizzata.

   ![](../assets/expression-assistant-pane.png)

1. Nel campo di testo, descrivi l’espressione da generare in linguaggio semplice. Ad esempio:

   * *&quot;Utenti dagli USA di età superiore a 18 anni&quot;*
   * *&quot;Clienti che hanno effettuato un acquisto negli ultimi 30 giorni&quot;*

   Consulta [Esempi di prompt](#example-prompts) alla fine di questa pagina per suggerimenti.

1. Fai clic su **[!UICONTROL Genera]** per inviare la richiesta.

   L’assistente inizia a generare l’espressione corrispondente e visualizza messaggi di stato di avanzamento mentre la generazione è in corso.

   >[!NOTE]
   >
   >Se l&#39;assistente non è in grado di generare un&#39;espressione valida, ad esempio se il prompt fa riferimento a campi che non esistono nelle origini dati disponibili, verrà visualizzato un messaggio di errore. In questo caso, modifica la richiesta di utilizzo dei nomi dei campi e delle origini dati disponibili nella configurazione del percorso, quindi genera di nuovo.

1. Quando l’espressione è pronta, rivedi il risultato nel pannello.

   ![](../assets/expression-assistant-result.png)

   * Fai clic sull&#39;icona ![Anteprima](../assets/do-not-localize/generation-preview.svg) prima di applicare per rivedere l&#39;output dell&#39;assistente per lo scenario richiesto.

   * Fai clic su **[!UICONTROL Applica]** per inserire l&#39;espressione generata direttamente nell&#39;editor di espressioni avanzate (nello stesso posizionamento in cui verrebbe incollata manualmente).
   * Utilizzare il controllo Copy per acquisire il testo dell&#39;espressione suggerita e incollarlo altrove, se necessario.

## Esempi di prompt {#example-prompts}

Gli elenchi seguenti sono solo spunti. Non mostrano la sintassi dell’espressione generata, l’output esatto dipende dai campi e dalle attività definite nel percorso.

### Evento di percorso e azione personalizzata {#example-prompts-event-action}

* *&quot;evento con prezzo totale ordine superiore a 100&quot;*
* *&quot;evento in cui l&#39;ordine è stato creato negli ultimi 7 giorni&quot;*
* *&quot;evento in cui il tipo di evento è un acquisto commerce&quot;*
* *&quot;evento con ordine creato nell&#39;ultima ora&quot;*
* *&quot;evento con prezzo totale ordine superiore a 200 e risposta azione con codice di stato&quot;*

### Espressioni dell’attività Attendi {#example-prompts-datetime}

Quando un&#39;attività **[!UICONTROL Wait]** utilizza una data personalizzata, è possibile definire quando il profilo continua creando un&#39;espressione `dateTimeOnly` nell&#39;**[!UICONTROL Editor espressioni avanzate]**. Ad esempio, da un attributo di profilo, una marca temporale evento, dati di qualificazione del segmento o un offset calcolato dall’ora corrente. Per informazioni su come configurare le attese personalizzate e i limiti applicabili, vedere [Attesa personalizzata](../wait-activity.md#custom).

* *&quot;usa la data dell&#39;ultimo ordine del cliente solo come data e ora&quot;*
* *&quot;usa l&#39;ora e-mail del consenso solo come data e ora&quot;*
* *&quot;convertire l&#39;iscrizione al segmento solo dall&#39;ultima qualifica all&#39;ora corrente&quot;*
* *&quot;nodo di attesa: una settimana dopo Natale 2024 come solo data e ora&quot;*
* *&quot;nodo di attesa: 30 giorni a partire da ora alle 22 solo come data/ora&quot;*
* *&quot;Attendere fino alle 9 di oggi in fuso orario UTC, restituire solo come data e ora&quot;*

## Risorse correlate {#related}

* [Utilizzare l&#39;editor di espressioni avanzato](expressionadvanced.md): panoramica dell&#39;interfaccia dell&#39;editor di espressioni e della sintassi supportata.
* [Introduzione all&#39;Assistente all&#39;intelligenza artificiale in Journey Optimizer](../../content-management/gs-generative.md): guardrail generali, accesso e configurazione per le funzionalità di intelligenza artificiale generative.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come utilizzare l&#39;intelligenza artificiale nell&#39;editor di espressioni avanzate di Percorso per generare espressioni di percorso valide dai prompt di linguaggio semplice.

**Intenti:**

* Generare un’espressione di percorso da una descrizione in linguaggio naturale utilizzando IA
* Applicare un’espressione generata direttamente nell’editor di espressioni avanzate con il pulsante Applica
* Utilizzare la generazione di espressioni basate sull’intelligenza artificiale nelle attività Ottimizza, Condizione e Attesa con data personalizzata
* Fornisci prompt di esempio per condizioni basate su eventi ed espressioni di attesa `dateTimeOnly`
* Risolvere i problemi di generazione non riuscita modificando i prompt per fare riferimento a nomi di campo e origini dati validi

**Glossario:**

* **Genera espressioni con IA**: funzionalità generativa basata su IA incorporata nell&#39;editor di espressioni avanzate di Percorso che converte i prompt del linguaggio semplice in espressioni di percorso valide *(specifiche del prodotto)*
* **Editor espressioni avanzate**: interfaccia di Journey Optimizer per la scrittura di espressioni complesse nelle condizioni, nelle attività di attesa e nella mappatura dei parametri delle azioni *(specifico per prodotto)*
* **dateTimeOnly**: tipo di espressione data-ora senza fuso orario, richiesto per le attività di attesa per data personalizzata *(specifiche per prodotto)*
* **Ottimizza attività**: attività di percorso che supporta le condizioni di diramazione configurabili tramite l&#39;editor di espressioni avanzate *(specifico per prodotto)*

**Guardrail:**

* Generare espressioni con IA è attualmente in **versione beta pubblica**. La disponibilità e il comportamento potrebbero cambiare
* A questa funzione si applicano i guardrail e le limitazioni di IA generativa riportati nella documentazione principale di AI Assistant
* Se l&#39;assistente fa riferimento a campi non presenti nelle origini dati del percorso, restituisce un errore. Per utilizzare i nomi di campo disponibili, modificare la richiesta.
* La sintassi esatta dell’espressione generata dipende dai campi e dalle attività configurate nel percorso specifico

**Terminologia:**

* Nome canonico: Genera espressioni con IA — Acronimo: none — Varianti: Generazione espressione IA, Generatore espressione percorso
* Sinonimi: &quot;Generare espressioni con IA&quot; = &quot;Generatore di espressioni AI&quot;
* Non confondere: Genera espressioni con AI (Generatore basato sull’intelligenza artificiale) ≠ Editor di espressioni avanzate (l’editor di codice manuale stesso)

**Domande frequenti:**

* **Q: dove è disponibile Generare espressioni con IA?** — è disponibile ovunque si apra l’editor di espressioni avanzate del Percorso, tra cui le attività Condizione, Ottimizza attività e Attendi con una data personalizzata.
* **D: cosa succede se AI non è in grado di generare un&#39;espressione valida?** — Viene visualizzato un messaggio di errore; è necessario modificare la richiesta per utilizzare i nomi dei campi e le origini dati esistenti nella configurazione del percorso.
* **D: come si inserisce un&#39;espressione generata nell&#39;editor?** — Fare clic sul pulsante **Applica** nel pannello assistente per inserirlo direttamente nella posizione corrente del cursore nell&#39;editor di espressioni avanzate.
* **Q: è possibile generare espressioni con IA per creare `dateTimeOnly` espressioni per le attività Attendi?** — Sì; ad esempio, se si richiede &quot;30 giorni a partire da ora alle 22 come solo data e ora&quot; viene generata l&#39;espressione `dateTimeOnly` appropriata.
* **Q: le espressioni di generazione con IA sono generalmente disponibili?** — No; è attualmente in versione beta pubblica. Per gli aggiornamenti sulla disponibilità, controlla la pagina del ciclo di rilascio di Journey Optimizer.

+++
