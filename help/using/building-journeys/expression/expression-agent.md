---
solution: Journey Optimizer
product: journey optimizer
title: Generare espressioni con l'Assistente espressioni
description: Scopri come utilizzare l’Assistente espressioni in Adobe Journey Optimizer per generare espressioni direttamente nell’editor di espressioni avanzate di Percorso utilizzando i prompt del linguaggio naturale.
feature: Journeys
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
badge: label="Beta pubblica" type="Informative"
mini-toc-levels: 2
hide: true
source-git-commit: 21019d3981891b2ea17857dfc15278641bbcb740
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 2%

---


# Generare espressioni con l&#39;Assistente espressioni {#expression-agent}

>[!CONTEXTUALHELP]
>id="journeyExpAI"
>title="Generare espressioni con l&#39;Assistente espressioni"
>abstract="L’Assistente espressioni utilizza l’intelligenza artificiale generativa per aiutarti a creare e generare espressioni direttamente nell’editor di espressioni avanzate di Percorso. Ad esempio, in condizioni, **Ottimizza** attività o **Attendi** attività che utilizzano una data personalizzata. Descrivi ciò di cui hai bisogno in linguaggio semplice e l’assistente genera l’espressione corrispondente per te."

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta pubblica**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](../../rn/releases.md).
>
>Prima di utilizzare l&#39;Assistente espressioni, leggere le [protezioni e limitazioni](../../content-management/gs-generative.md#generative-guardrails) correlate che si applicano alle funzionalità di IA generativa in Journey Optimizer.

L’Assistente espressioni è una funzione basata sull’intelligenza artificiale incorporata nell’editor di espressioni avanzate di Percorso. Consente di generare espressioni valide da prompt in linguaggio semplice.

È disponibile ovunque si apra l&#39;editor di espressioni avanzate **del Percorso.** Ad esempio, quando configuri condizioni e routing all&#39;interno di un&#39;attività **[Ottimizza](../optimize.md)** o quando configuri un&#39;attività [**[!UICONTROL Attendi &#x200B;]**](../wait-activity.md) che utilizza una data personalizzata e hai bisogno di un&#39;espressione `dateTimeOnly`.

## Generare un’espressione {#generate}

Per generare un&#39;espressione utilizzando l&#39;Assistente espressioni:

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
