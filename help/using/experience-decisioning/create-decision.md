---
title: Creare criteri di decisioni
description: Scopri come creare criteri di decisioni
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: 0b7f76ca43ef8dda3861abf2c3b058cef725e967
workflow-type: tm+mt
source-wordcount: '1715'
ht-degree: 11%

---

# Creare criteri di decisione {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Che cos’è una decisione?"
>abstract="I criteri di decisione contengono tutta la logica di selezione affinché il motore decisionale possa scegliere il contenuto migliore. I criteri di decisione sono specifici della campagna. Il loro obiettivo è selezionare le migliori offerte per ciascun profilo mentre la creazione della campagna consente di indicare come devono essere presentati gli elementi decisionali selezionati, inclusi gli attributi degli elementi da includere nel messaggio."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Informazioni sulla funzione Decisioni"

I criteri di decisione sono contenitori per le offerte che sfruttano il motore di decisione per scegliere il contenuto migliore da distribuire, a seconda del pubblico.

<!--Decision policies contain all of the selection logic for the decisioning engine to pick the best content. Decision policies are campaign specific. -->Il loro obiettivo è quello di selezionare le offerte migliori per ciascun profilo, mentre l’authoring della campagna/del percorso ti consente di indicare in che modo devono essere presentati gli elementi decisionali selezionati, compresi gli attributi degli elementi da includere nel messaggio.

>[!NOTE]
>
>Nell&#39;interfaccia utente [!DNL Journey Optimizer], i criteri di decisione sono etichettati come decisioni<!--but they are decision policies. TBC if this note is needed-->.

I passaggi principali per sfruttare i criteri decisionali nelle campagne basate su codice sono i seguenti:

1. [Aggiungere un criterio di decisione a un’esperienza basata su codice](#add-decision)
1. [Utilizzare il criterio di decisione](#use-decision-policy)
1. [Creare dashboard di reporting personalizzati per Customer Journey Analytics](cja-reporting.md)

## Aggiungere un criterio di decisione a un’esperienza basata su codice {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="Definire il numero di elementi da restituire"
>abstract="Seleziona il numero di elementi decisionali che desideri restituire. Ad esempio, se selezioni 2, verranno presentate le 2 offerte idonee migliori per la configurazione corrente."

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="Selezionare un fallback"
>abstract="L’utente visualizza un elemento di fallback quando nessuna delle strategie di selezione definite per tale criterio decisionale è qualificata."

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="Che cos’è una strategia?"
>abstract="La sequenza della strategia di selezione determina quale strategia verrà valutata per prima. È necessaria almeno una strategia. Gli elementi decisionali nelle strategie combinate saranno valutati insieme."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Creare strategie"

Per presentare l’offerta e l’esperienza migliore e dinamica ai visitatori sul sito web o sull’app mobile, aggiungi un criterio decisionale a una campagna o a un percorso basato su codice. A questo scopo, segui i passaggi riportati qui sotto.

### Creare il criterio di decisione {#add}

1. Crea una campagna e seleziona l&#39;azione **[!UICONTROL Esperienza basata su codice]**. [Ulteriori informazioni](../code-based/create-code-based.md)

1. Dall&#39;[editor di codice](../code-based/create-code-based.md#edit-code), selezionare **[!UICONTROL Criterio decisione]** e fare clic su **[!UICONTROL Aggiungi criterio decisione]**.

   ![](assets/decision-code-based-create.png)

1. Per impostazione predefinita, crea un nuovo criterio.

   >[!NOTE]
   >
   >Puoi anche scegliere di selezionare un criterio esistente.

1. Inserisci i dettagli del criterio di decisione: aggiungi un nome e seleziona un catalogo.

   >[!NOTE]
   >
   >Attualmente è disponibile solo il catalogo predefinito **[!UICONTROL Offerte]**.

1. Selezionare il numero di elementi che si desidera restituire. Ad esempio, se selezioni 2, verranno presentate le migliori 2 offerte idonee per la configurazione corrente. Fai clic su **[!UICONTROL Avanti]**.

   ![](assets/decision-code-based-details.png)

### Selezione di elementi e strategie di selezione {#select}

La sezione **[!UICONTROL Sequenza strategica]** consente di selezionare gli elementi decisionali e le strategie di selezione da presentare con il criterio decisionale.

1. Fai clic sul pulsante **[!UICONTROL Aggiungi]**.

1. Scegliere il tipo di oggetto da includere nel criterio:

   * **[!UICONTROL Strategia di selezione]**: aggiungere una o più strategie di selezione. Le strategie decisionali sfruttano le raccolte associate ai vincoli di idoneità e ai metodi di classificazione per determinare gli elementi da mostrare. Puoi selezionare una strategia di selezione esistente o crearne una nuova utilizzando il pulsante **[!UICONTROL Crea strategia di selezione]**. [Scopri come creare strategie di selezione](selection-strategies.md)

   * **[!UICONTROL Elemento decisione]**: aggiungere singoli elementi decisione da presentare senza dover eseguire una strategia di selezione. È possibile selezionare un solo elemento di decisione alla volta. Eventuali vincoli di idoneità impostati per l’articolo verranno applicati.

   ![](assets/decision-code-based-strategy-sequence.png)

   >[!NOTE]
   >
   >Una politica decisionale supporta fino a 10 strategie di selezione e elementi decisionali combinati. [Ulteriori informazioni su guardrail e limitazioni di Decisioning](gs-experience-decisioning.md#guardrails)

1. Quando si aggiungono più elementi e/o strategie di decisione, queste vengono valutate in un ordine specifico. Il primo oggetto aggiunto alla sequenza verrà valutato per primo e così via.

   Per modificare la sequenza predefinita, è possibile trascinare e rilasciare gli oggetti e/o i gruppi per riordinarli in base alle esigenze. [Ulteriori informazioni](#evaluation-order)

### Gestire l’ordine di valutazione in un criterio decisionale {#evaluation-order}

Dopo aver aggiunto al criterio elementi decisionali e strategie di selezione, è possibile disporne l&#39;ordine per determinarne l&#39;ordine di valutazione e combinare le strategie di selezione per valutarli insieme.

L&#39;**ordine sequenziale** in cui verranno valutati gli elementi e le strategie è indicato con numeri alla sinistra di ogni oggetto o gruppo di oggetti. Per spostare la posizione di una strategia di selezione (o di un gruppo di strategie) all&#39;interno della sequenza, trascinarla e rilasciarla in un&#39;altra posizione.

>[!NOTE]
>
>Solo le strategie di selezione possono essere trascinate e rilasciate all&#39;interno di una sequenza. Per modificare la posizione di un elemento di decisione, è necessario rimuoverlo e aggiungerlo nuovamente utilizzando il pulsante **[!UICONTROL Aggiungi]** dopo aver aggiunto gli altri elementi che si desidera valutare in precedenza.

![](assets/decision-code-based-strategy-groups.png)

È inoltre possibile **combinare** più strategie di selezione in gruppi in modo che vengano valutate insieme e non separatamente. A tale scopo, fare clic sul pulsante **`+`** in una strategia di selezione per combinarla con un&#39;altra. Puoi anche trascinare e rilasciare una strategia di selezione su un’altra per raggruppare le due strategie in un gruppo.

>[!NOTE]
>
>Gli elementi decisionali non possono essere raggruppati con altri elementi o strategie di selezione.

Le strategie multiple e il loro raggruppamento determinano la priorità delle strategie e la classificazione delle offerte idonee. La prima strategia ha la massima priorità e le strategie combinate all&#39;interno dello stesso gruppo hanno la stessa priorità.

Ad esempio, sono disponibili due raccolte, una nella strategia A e una nella strategia B. La richiesta prevede il rinvio di due elementi decisionali. Supponiamo che vi siano due offerte ammissibili dalla strategia A e tre offerte ammissibili dalla strategia B.

* Se le due strategie sono **non combinate** o in ordine sequenziale (1 e 2), le prime due offerte idonee della prima strategia verranno restituite nella prima riga. Se non ci sono due offerte idonee per la prima strategia, il motore decisionale passerà alla strategia successiva in sequenza per trovare quante offerte sono ancora necessarie e alla fine restituirà un fallback, se necessario.

  ![](assets/decision-code-based-consecutive-strategies.png)

* Se le due raccolte sono **valutate contemporaneamente**, poiché esistono due offerte idonee dalla strategia A e tre offerte idonee dalla strategia B, le cinque offerte saranno tutte raggruppate in base al valore determinato dai rispettivi metodi di classificazione. Sono richieste due offerte, pertanto verranno restituite le prime due offerte idonee di queste cinque.

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

Offerta 1 - 10
Offerta 2 - 20
Offerta 3-30 dalla Strategia 1, 45 dalla Strategia 2. Il più alto di entrambi sarà considerato, quindi 45 è preso in considerazione.
Offerta 4 - 40
Offerta 5 - 50

Le offerte classificate sono ora le seguenti: Offerta 5, Offerta 3, Offerta 4, Offerta 2, Offerta 1.

**Iterazione 2:**

Vengono valutate le offerte della Strategia 3 (Offerta 5, Offerta 6). Supponiamo che il risultato sia:

* Offerta 5: non verrà valutata perché esiste già nel risultato precedente.
* Offerta 6 - 60

Le offerte classificate sono ora le seguenti: Offerta 5 , Offerta 3, Offerta 4, Offerta 2, Offerta 1, Offerta 6.

+++

### Aggiungere offerte di fallback {#fallback}

Dopo aver selezionato elementi decisionali e/o strategie di selezione, puoi aggiungere offerte di fallback che verranno visualizzate dagli utenti se nessuno degli elementi o strategie di selezione di cui sopra è qualificato.

![](assets/decision-code-based-strategy-fallback.png)

È possibile selezionare qualsiasi elemento dall’elenco, in cui vengono visualizzati tutti gli elementi decisionali creati nella sandbox corrente. Se non viene definita alcuna strategia di selezione, il fallback viene visualizzato all&#39;utente indipendentemente dalle date e dal vincolo di idoneità applicato all&#39;elemento selezionato<!--nor frequency capping when available - TO CLARIFY-->.

>[!NOTE]
>
>Un fallback è facoltativo. Se non è selezionato alcun fallback e nessuna strategia è qualificata, [!DNL Journey Optimizer] non visualizzerà nulla. Puoi aggiungere fino al numero di elementi richiesti dal criterio di decisione. In questo modo viene garantito un determinato numero di elementi da restituire, se desiderato per il caso d’uso.

Quando il criterio decisionale è pronto, salvarlo e fare clic su **[!UICONTROL Crea]**. Dopo aver creato il criterio decisionale, puoi utilizzare gli attributi di decisione all’interno del contenuto dell’esperienza basata su codice. [Ulteriori informazioni](#use-decision-policy)

![](assets/decision-code-based-decision-added.png)

## Utilizzare il criterio di decisione nell’editor di codice {#use-decision-policy}

Una volta creato, il criterio di decisione può essere utilizzato nell&#39;[editor di personalizzazione](../code-based/create-code-based.md#edit-code). A questo scopo, segui i passaggi riportati qui sotto.

>[!NOTE]
>
>L&#39;esperienza basata su codice sfrutta l&#39;editor di personalizzazione [!DNL Journey Optimizer] con tutte le sue funzionalità di personalizzazione e authoring. [Ulteriori informazioni](../personalization/personalization-build-expressions.md)

1. Fare clic sul pulsante **[!UICONTROL Inserisci criterio]**. Viene aggiunto il codice corrispondente al criterio di decisione.

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >Questa sequenza verrà ripetuta il numero di volte che si desidera che venga restituito il criterio di decisione. Ad esempio, se si sceglie di restituire 2 elementi durante la [creazione della decisione](#add-decision), la stessa sequenza verrà ripetuta due volte.

1. Ora puoi aggiungere tutti gli attributi di decisione desiderati all’interno di tale codice. Gli attributi disponibili sono archiviati nello schema del catalogo **[!UICONTROL Offerte]**. Gli attributi personalizzati sono archiviati nella cartella **`_<imsOrg`>** e gli attributi standard nella cartella **`_experience`**. [Ulteriori informazioni sullo schema del catalogo delle offerte](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

   >[!NOTE]
   >
   >Per il tracciamento degli elementi dei criteri di decisione, è necessario aggiungere l&#39;attributo `trackingToken` come segue per il contenuto dei criteri di decisione:
   >`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. Fai clic su ciascuna cartella per espanderla. Posizionare il cursore del mouse nella posizione desiderata e fare clic sull&#39;icona + accanto all&#39;attributo che si desidera aggiungere. Puoi aggiungere al codice tutti gli attributi che desideri.

   ![](assets/decision-code-based-add-decision-attributes.png)

1. Puoi anche aggiungere qualsiasi altro attributo disponibile nell’editor di personalizzazione, ad esempio gli attributi del profilo.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Fai clic su **[!UICONTROL Salva e chiudi]** per confermare le modifiche.

1. Rivedi e pubblica la campagna o il percorso di esperienze basato su codice. [Scopri come](../code-based/publish-code-based.md)

   Ora, non appena lo sviluppatore effettua una chiamata API o SDK per recuperare il contenuto per la superficie definita nella configurazione del canale, le modifiche verranno applicate alla pagina web o all’app.

   >[!NOTE]
   >
   >Attualmente non è possibile simulare contenuti dall&#39;interfaccia utente in una campagna o in un percorso [esperienza basata su codice](../code-based/create-code-based.md) utilizzando le decisioni. Una soluzione alternativa è disponibile in [questa sezione](../code-based/code-based-decisioning-implementations.md).

1. Per visualizzare le prestazioni delle decisioni, puoi creare [dashboard di reporting di Customer Journey Analytics](cja-reporting.md) personalizzati.


