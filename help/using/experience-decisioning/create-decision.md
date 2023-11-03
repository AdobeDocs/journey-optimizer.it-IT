---
title: Creare decisioni
description: Scopri come creare decisioni
feature: Experience Decisioning
topic: Integrations
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 20%

---

# Creare criteri di decisione {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Che cos’è una decisione?"
>abstract="I criteri decisionali sfruttano il motore di Offer Decisioning per scegliere i contenuti migliori da distribuire in base al pubblico."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=it" text="Informazioni su Offer Decisioning"

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* [Introduzione a Offer Decisioning](gs-experience-decisioning.md)
* Gestire gli elementi decisionali
   * [Configurare il catalogo degli elementi](catalogs.md)
   * [Creare elementi decisionali](items.md)
   * [Gestire le raccolte di elementi](collections.md)
* Configurare la selezione degli elementi
   * [Creare regole di decisione](rules.md)
   * [Creare metodi di classificazione](ranking.md)
* [Creare strategie di selezione](selection-strategies.md)
* **[Creare criteri di decisione](create-decision.md)**

>[!ENDSHADEBOX]

I criteri di decisione sono contenitori per le offerte che sfruttano il motore di experience decisioning per scegliere il contenuto migliore da distribuire, a seconda del pubblico.

>[!NOTE]
>
>In [!DNL Journey Optimizer] interfaccia utente, i criteri di decisione sono etichettati come decisioni<!--but they are decision policies. TBC if this note is needed-->.

## Aggiungere un criterio di decisione a una campagna basata sul codice {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Definire il numero di elementi da restituire"
>abstract="Seleziona il numero di elementi decisionali che desideri restituire. Ad esempio, se selezioni 2, verranno presentate le 2 offerte idonee migliori per la superficie corrente."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Selezionare un fallback"
>abstract="L’utente visualizza un elemento di fallback quando nessuna delle strategie di selezione definite per tale criterio decisionale è qualificata."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="Che cos’è una strategia?"
>abstract="La sequenza della strategia di selezione determina quale strategia verrà valutata per prima. È necessaria almeno una strategia. Gli elementi decisionali nelle strategie combinate saranno valutati insieme."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=it" text="Creare strategie"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html?lang=it" text="Ordine di valutazione"

Per presentare l’offerta e l’esperienza migliore e dinamica ai visitatori sul sito web o sull’app mobile, aggiungi un criterio decisionale a una campagna basata su codice. A questo scopo, segui i passaggi riportati qui sotto.

1. Crea una campagna e seleziona la **[!UICONTROL Esperienza basata su codice (Beta)]** azione. [Ulteriori informazioni](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >La funzione di esperienza basata su codice è attualmente disponibile come versione beta solo per alcuni utenti.

1. Dalla sezione [editor di codice](../code-based/create-code-based.md#edit-code), seleziona la **[!UICONTROL Decisioni]** e fai clic su **[!UICONTROL Creare una decisione]**.

   ![](assets/decision-code-based-create.png)

1. Inserisci i dettagli del criterio di decisione: aggiungi un nome e seleziona un catalogo.

   >[!NOTE]
   >
   >Attualmente solo il valore predefinito **[!UICONTROL Offerte]** il catalogo è disponibile.

   ![](assets/decision-code-based-details.png)

1. Selezionare il numero di elementi che si desidera restituire. Ad esempio, se selezioni 2, verranno presentate le 2 offerte idonee migliori per la superficie corrente. Fai clic su **[!UICONTROL Avanti]**

1. Utilizza il **[!UICONTROL Aggiungi strategia]** per definire le strategie di selezione per il criterio di decisione. Ogni strategia consiste in una raccolta di offerte associata a un vincolo di idoneità e a un metodo di classificazione per determinare le offerte da visualizzare. [Ulteriori informazioni](selection-strategies.md)

   ![](assets/decision-code-based-strategies.png)

   >[!NOTE]
   >
   >È necessaria almeno una strategia. Impossibile aggiungere più di 10 strategie.

1. Dalla sezione **[!UICONTROL Aggiungi strategia]** , puoi anche creare una strategia. Il **[!UICONTROL Creare una strategia di selezione]** reindirizzamento al pulsante **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Configurazioni]** menu. [Ulteriori informazioni](selection-strategies.md)

   ![](assets/decision-code-based-add-strategy.png)

1. Quando si aggiungono più strategie, queste verranno valutate in un ordine specifico. La prima strategia aggiunta alla sequenza verrà valutata per prima e così via. [Ulteriori informazioni](#evaluation-order)

   Per modificare la sequenza predefinita, puoi trascinare e rilasciare le strategie e/o i gruppi per riordinarli come desiderato.

   ![](assets/decision-code-based-strategy-groups.png)

1. Aggiungi un fallback. Se nessuna delle strategie di selezione di cui sopra è qualificata, viene visualizzato un elemento di fallback.

   ![](assets/decision-code-based-strategy-fallback.png)

   È possibile selezionare qualsiasi elemento dall’elenco, in cui vengono visualizzati tutti gli elementi decisionali creati nella sandbox corrente. Se non viene definita alcuna strategia di selezione, il fallback viene visualizzato all’utente indipendentemente dalle date e dal vincolo di idoneità applicato all’elemento selezionato<!--nor frequency capping when available - TO CLARIFY-->.

   >[!NOTE]
   >
   >Un fallback è facoltativo. Se non è selezionato alcun fallback e non è stata qualificata alcuna strategia, non viene visualizzato nulla da [!DNL Journey Optimizer].

1. Salva la selezione e fai clic su **[!UICONTROL Crea]**. La nuova politica decisionale è aggiunta in **[!UICONTROL Decisioni]**.

   ![](assets/decision-code-based-decision-added.png)

Dopo aver creato il criterio decisionale, puoi utilizzare gli attributi di decisione all’interno del contenuto dell’esperienza basata su codice. [Ulteriori informazioni](#use-decision-policy)

## Ordine di valutazione {#evaluation-order}

Come descritto in precedenza, una strategia è costituita da una raccolta, un metodo di classificazione e vincoli di idoneità.

Puoi eseguire le seguenti operazioni:

* Impostare l&#39;ordine sequenziale desiderato per la valutazione delle strategie,
* Combinare più strategie in modo che vengano valutate insieme e non separatamente.

Le strategie multiple e il loro raggruppamento determinano la priorità delle strategie e la classificazione delle offerte idonee. La prima strategia ha la massima priorità e le strategie combinate all&#39;interno dello stesso gruppo hanno la stessa priorità.

Ad esempio, sono disponibili due raccolte, una nella strategia A e una nella strategia B. La richiesta prevede il rinvio di due elementi decisionali. Supponiamo che vi siano due offerte ammissibili dalla strategia A e tre offerte ammissibili dalla strategia B.

* Se le due strategie sono **non combinato** oppure in ordine sequenziale (1 e 2), le prime due offerte idonee della prima strategia verranno restituite nella prima riga. Se non ci sono due offerte idonee per la prima strategia, il motore decisionale passerà alla strategia successiva in sequenza per trovare quante offerte sono ancora necessarie e alla fine restituirà un fallback, se necessario.

  ![](assets/decision-code-based-consecutive-strategies.png)

* Se le due raccolte sono **valutato contemporaneamente** Poiché esistono due offerte ammissibili della strategia A e tre offerte ammissibili della strategia B, le cinque offerte saranno tutte raggruppate in base al valore determinato dai rispettivi metodi di classificazione. Sono richieste due offerte, pertanto verranno restituite le prime due offerte idonee di queste cinque.

  ![](assets/decision-code-based-combined-strategies.png)

+++ **Esempio con più strategie**

Prendiamo ora in considerazione un esempio in cui si dispone di più strategie suddivise in gruppi diversi.

Hai definito tre strategie. La strategia 1 e la strategia 2 sono combinate nel gruppo 1 e la strategia 3 è indipendente (gruppo 2).

Le offerte ammissibili per ciascuna strategia e la loro priorità (utilizzata nella valutazione della funzione di classificazione) sono le seguenti:

* Gruppo 1:
   * Strategia 1 - (offerta 1, offerta 2, offerta 3) - Priorità 1
   * Strategia 2 - (offerta 3, offerta 4, offerta 5) - Priorità 1

* Gruppo 2:
   * Strategia 3 - (Offerta 5, Offerta 6) - Priorità 0

Le offerte di strategia con priorità più alta vengono valutate per prime e aggiunte all’elenco delle offerte classificate.

**Iterazione 1:**

Le offerte di Strategia 1 e Strategia 2 vengono valutate insieme (Offerta 1, Offerta 2, Offerta 3, Offerta 4, Offerta 5). Supponiamo che il risultato sia:

Offerta 1 - 10 Offerta 2 - 20 Offerta 3 - 30 dalla strategia 1, 45 dalla strategia 2. Il più alto di entrambi sarà considerato, quindi 45 è preso in considerazione.
Offerta 4 - 40 Offerta 5 - 50

Le offerte classificate sono ora le seguenti: Offerta 5, Offerta 3, Offerta 4, Offerta 2, Offerta 1.

**Iterazione 2:**

Vengono valutate le offerte della Strategia 3 (Offerta 5, Offerta 6). Supponiamo che il risultato sia:

* Offerta 5: non verrà valutata perché esiste già nel risultato precedente.
* Offerta 6 - 60

Le offerte classificate sono ora le seguenti: Offerta 5 , Offerta 3, Offerta 4, Offerta 2, Offerta 1, Offerta 6.

+++

## Utilizzare il criterio di decisione nell’editor di codice {#use-decision-policy}

Una volta creato, il criterio di decisione può essere utilizzato nel [Editor espressioni](../code-based/create-code-based.md#edit-code). A questo scopo, segui i passaggi riportati qui sotto.

>[!NOTE]
>
>L&#39;esperienza basata su codice sfrutta [!DNL Journey Optimizer] Editor espressioni con tutte le sue funzionalità di personalizzazione e authoring. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

1. Fai clic sull’icona +. Viene aggiunto il codice corrispondente al criterio di decisione. Ora puoi aggiungere tutti gli attributi di decisione desiderati all’interno di tale codice.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Questa sequenza verrà ripetuta il numero di volte che si desidera che venga restituito il criterio di decisione. Ad esempio, se scegli di restituire indietro 2 elementi quando [creazione della decisione](#add-decision), la stessa sequenza verrà ripetuta due volte.

1. Fai clic sul criterio di decisione. Vengono visualizzati gli attributi di decisione.

   Questi attributi vengono memorizzati nel **[!UICONTROL Offerte]** schema del catalogo. Gli attributi personalizzati sono memorizzati in **`_<imsOrg`>** cartella e attributi standard nella **`_experience`** cartella. [Ulteriori informazioni sullo schema del catalogo delle offerte](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

1. Fai clic su ciascuna cartella per espanderla. Posizionare il cursore del mouse nella posizione desiderata e fare clic sull&#39;icona + accanto all&#39;attributo che si desidera aggiungere. Puoi aggiungere al codice tutti gli attributi che desideri.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Per tornare alla directory principale dei criteri di decisione, fai clic sull’icona della cartella.

   ![](assets/decision-code-based-decision-folder.png)

1. Puoi anche aggiungere qualsiasi altro attributo disponibile nell’editor espressioni, ad esempio gli attributi del profilo.

   ![](assets/decision-code-based-decision-profile-attribute.png)
