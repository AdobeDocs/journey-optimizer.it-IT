---
title: Create decisions policies
description: Learn how to create decisions policies
feature: Decisioning
topic: Integrations
role: User
level: Experienced
version: Journey Orchestration
exl-id: e7a89354-28ea-431f-a15d-a8c18946d266
source-git-commit: 1ee6f9d74b83ca2b9c2cc0336af0f23a42f4da4f
workflow-type: tm+mt
source-wordcount: '2257'
ht-degree: 6%

---

# Creare criteri di decisione {#create-decision}

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

To present the best dynamic offer and experience to your customers, add a decision policy to your content in a campaign or journey then configure the items to return and the selection strategy to use. A questo scopo, segui i passaggi riportati qui sotto:

1. [Add a decision policy](#add)
1. [Configure the decision policy](#configure) - Add a name and specify the number of items to return for the email channel.
1. [Set up a strategy sequence](#strategy) - Select the items to return with the decision policy.
1. [Select fallback offers](#fallback) (optional) - Select items to display if no items or selection strategies are qualified.
1. [Review and save](#review) the selection strategy
1. [Assign a placement](#placement) (Email channel only)

>[!AVAILABILITY]
>
>Decision policies are available for the **Code-based Experience**, **Push notification**, **SMS**, and **Email** channels.

## Add a decision policy {#add}

Open a journey or campaign, select a [channel action](../building-journeys/journey-action.md) and edit the content of your message.

Edit the content of your message and browse the tabs below for more information on how to add the decision policy based on the selected channel.

>[!BEGINTABS]

>[!TAB Esperienza basata su codice]

For code-based experiences, you can add a new decision policy using either the **code editor**, or the **Decisioning** menu available in the properties pane.

+++Add a decision policy from the code editor

1. Open the code editor editor using the **[!UICONTROL Edit code]** button.

1. Navigate to the **[!UICONTROL Decision policy]** menu then click the **[!UICONTROL Add decision policy]** button.

   ![](assets/decision-policy-add-code-editor.png)

+++

+++Add a decison policy from the Decisioning menu

1. Click the ![](assets/do-no-localize/decisioning-icon.png) icon from the properties pane to access the **[!UICONTROL Decisioning]** menu.

1. Click the **[!UICONTROL Add decision policy]** button.

   ![](assets/decision-policy-add-code.png)

+++

>[!TAB E-mail]

1. Toggle the **[!UICONTROL Enable decisioning]** option.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >Enabling decisioning clears existing email content. Se hai già progettato l’e-mail, assicurati di salvare preventivamente il contenuto come modello.

1. Aggiungi un nuovo criterio di decisione utilizzando l&#39;**editor di personalizzazione** o il menu **Decisioning** disponibile in E-mail Designer.

   +++Aggiungere un criterio di decisione dall’editor di Personalization

   1. Apri l&#39;editor di personalizzazione utilizzando l&#39;icona ![](assets/do-no-localize/editor-icon.svg) disponibile nel campo dell&#39;oggetto o in qualsiasi campo del corpo dell&#39;e-mail in cui puoi aggiungere la personalizzazione.

   1. Passa al menu **[!UICONTROL Criteri di decisione]**, quindi fai clic sul pulsante **[!UICONTROL Aggiungi criterio di decisione]**.

      ![](assets/decision-policy-add-email-editor.png)

   +++

   +++Aggiungere un criterio di decisione dal menu Decisioning

   1. Apri E-mail Designer e seleziona un componente nella struttura dell’e-mail.

   1. Fare clic sull&#39;icona ![](assets/do-no-localize/decisioning-icon.png) nel riquadro delle proprietà per accedere al menu **[!UICONTROL Decisioning]**.

   1. Fare clic sul pulsante **[!UICONTROL Aggiungi nuovo criterio]**.

      ![](assets/decision-policy-add-email-add.png)

   >[!NOTE]
   >
   >L&#39;opzione **[!UICONTROL Riutilizza output decisione]** consente di riutilizzare un criterio di decisione già creato in questa e-mail. È particolarmente utile quando desideri mostrare la stessa offerta in più posizioni (ad esempio, intestazione e piè di pagina).
   >
   >Quando la stessa offerta può essere selezionata da più di un criterio di decisione nel corpo dell’e-mail, il motore deduplica le offerte: ogni posizionamento riceve un’offerta diversa, pertanto la stessa offerta non verrà visualizzata in entrambe le posizioni. Per visualizzare la stessa offerta in più posizionamenti, utilizza **[!UICONTROL Riutilizza output decisione]** per riutilizzare l&#39;output di un criterio di decisione esistente in questa e-mail.

   +++

Puoi anche aggiungere criteri di decisione quando utilizzi la modalità **[!UICONTROL Crea un codice personalizzato]** in E-mail Designer. A tale scopo, passare a **[!UICONTROL Criteri di decisione]** per inserire il codice dei criteri di decisione. [Scopri come programmare il contenuto delle e-mail](../email/code-content.md).

![](assets/decision-policy-add-code-your-own.png)

>[!NOTE]
>
>In modalità **[!UICONTROL Crea il codice per te]**, puoi restituire solo un elemento decisione per criterio, perché il componente **[!UICONTROL Ripeti griglia]** non è disponibile.

>[!TAB SMS]

Per SMS, puoi aggiungere un nuovo criterio di decisione utilizzando l&#39;**editor di personalizzazione** o il menu **Decisioning** disponibile nel riquadro delle proprietà.

+++Aggiungere un criterio di decisione dall’editor di personalizzazione

1. Apri l&#39;editor di personalizzazione utilizzando l&#39;icona ![](assets/do-no-localize/editor-icon.svg).
1. Passa al menu **[!UICONTROL Criteri di decisione]**, quindi fai clic sul pulsante **[!UICONTROL Aggiungi criterio di decisione]**.

   ![](assets/decision-policy-add-sms-editor.png)

+++

+++Aggiungere un criterio di decisione dal menu Decisioning

1. Fare clic sull&#39;icona ![](assets/do-no-localize/decisioning-icon.png) nel riquadro delle proprietà per accedere al menu **[!UICONTROL Decisioning]**.

1. Fare clic sul pulsante **[!UICONTROL Aggiungi criterio di decisione]**.

   ![](assets/decision-policy-add-sms.png)

+++

>[!TAB Notifica push]

Per le notifiche push, puoi aggiungere un nuovo criterio di decisione utilizzando l&#39;**editor di personalizzazione** o il menu **Decisioning** disponibile nel riquadro delle proprietà.

+++Aggiungere un criterio di decisione dall’editor di personalizzazione

1. Apri l&#39;editor di personalizzazione utilizzando l&#39;icona ![](assets/do-no-localize/editor-icon.svg).
1. Passa al menu **[!UICONTROL Criteri di decisione]**, quindi fai clic sul pulsante **[!UICONTROL Aggiungi criterio di decisione]**.

   ![](assets/decision-policy-add-push.png)

+++

+++Aggiungere un criterio di decisione dal menu Decisioning

1. Fare clic sull&#39;icona ![](assets/do-no-localize/decisioning-icon.png) nel riquadro delle proprietà per accedere al menu **[!UICONTROL Decisioning]**.

1. Fare clic sul pulsante **[!UICONTROL Aggiungi criterio di decisione]**.

   ![](assets/decision-policy-add-push-menu.png)

>[!IMPORTANT]
>
>Experience Decisioning con notifiche push richiede una versione specifica del SDK mobile. Prima di implementare questa funzione, controlla le [note sulla versione](https://developer.adobe.com/client-sdks/home/release-notes){target="_blank"} per identificare la versione richiesta e assicurarti di aver effettuato l&#39;aggiornamento di conseguenza. Puoi anche visualizzare tutte le versioni di SDK disponibili per la tua piattaforma in [questa sezione](https://developer.adobe.com/client-sdks/home/current-sdk-versions){target="_blank"}.

+++

>[!ENDTABS]

## Configurare il criterio di decisione {#configure}

Dopo aver aggiunto un nuovo criterio di decisione al contenuto, viene visualizzata la schermata di configurazione del criterio di decisione. Per configurare i criteri di decisione, segui la procedura riportata di seguito.

1. Specifica un nome per il criterio di decisione e seleziona un catalogo (attualmente limitato al catalogo predefinito **[!UICONTROL Offerte]**).

   ![](assets/decision-code-based-details.png)

1. Il campo **[!UICONTROL Numero di elementi]** consente di definire il numero di elementi decisionali da restituire con i criteri di decisione. Ad esempio, se selezioni 2, verranno presentate le 2 offerte idonee migliori per la configurazione corrente.

   >[!NOTE]
   >
   >Questa opzione è disponibile solo per i canali di esperienza basati su e-mail e codice. Per tutti gli altri canali, può essere restituito solo 1 elemento di decisione per azione.

   Per restituire più elementi per il canale e-mail, devi aggiungere il criterio di decisione all&#39;interno di un componente **[!UICONTROL Ripeti griglia]**. Per ulteriori informazioni, espandi la sezione seguente:

   +++Restituire più elementi decisionali nelle e-mail

   1. Trascina un componente **[!UICONTROL Ripeti griglia]** nell&#39;e-mail e configuralo come desiderato utilizzando il riquadro **[!UICONTROL Impostazioni]**.

      ![](assets/decision-policy-repeat.png)

   1. Fai clic sull&#39;icona **[!UICONTROL Decisioning]** nella barra degli strumenti dell&#39;area di lavoro oppure apri il riquadro **[!UICONTROL Decisioning]** e seleziona **[!UICONTROL Aggiungi criterio di decisione]**.

   1. Specifica il numero di elementi da restituire nel campo **[!UICONTROL Numero di elementi]**, quindi configura il criterio di decisione come documentato di seguito. Il numero massimo di elementi selezionabili è limitato dal numero di riquadri definito nel componente **[!UICONTROL Ripeti griglia]**.

   ![](assets/decision-policy-repeat-number.png)

   +++

1. Fai clic su **[!UICONTROL Avanti]**.

## Impostare una sequenza strategica {#strategy}

La sezione **[!UICONTROL Sequenza strategica]** consente di selezionare gli elementi decisionali e impostare strategie di selezione da presentare con il criterio decisionale.

1. Fare clic su **[!UICONTROL Aggiungi]** e scegliere il tipo di oggetto da includere nel criterio:

   ![](assets/decision-code-based-strategy-sequence.png)

   * **[!UICONTROL Strategia di selezione]** - Le strategie decisionali sfruttano le raccolte associate ai vincoli di idoneità e ai metodi di classificazione per determinare gli elementi da visualizzare. Puoi selezionare una o più strategie di selezione esistenti o crearne una nuova utilizzando il pulsante **[!UICONTROL Crea strategia di selezione]**. [Scopri come creare strategie di selezione](selection-strategies.md)

   * **[!UICONTROL Elemento decisione]** - Selezionare singoli elementi decisione senza dover eseguire una strategia di selezione. È possibile selezionare un solo elemento di decisione alla volta. Eventuali vincoli di idoneità impostati per l’articolo verranno applicati.

   >[!NOTE]
   >
   >Una politica decisionale supporta fino a 10 strategie di selezione e elementi decisionali combinati. [Ulteriori informazioni su guardrail e limitazioni di Decisioning](gs-experience-decisioning.md#guardrails)

1. Quando si aggiungono più elementi e/o strategie di decisione, queste vengono valutate in un ordine specifico. Il primo oggetto aggiunto alla sequenza verrà valutato per primo e così via. Per modificare la sequenza predefinita, trascinare e rilasciare gli oggetti e/o i gruppi per riordinarli in base alle esigenze. Espandi la sezione seguente per ulteriori dettagli.

   +++Gestire l’ordine di valutazione in un criterio decisionale

   Dopo aver aggiunto al criterio elementi decisionali e strategie di selezione, è possibile disporne l&#39;ordine per determinarne l&#39;ordine di valutazione e combinare le strategie di selezione per valutarli insieme.

   L&#39;**ordine sequenziale** in cui verranno valutati gli elementi e le strategie è indicato con numeri alla sinistra di ogni oggetto o gruppo di oggetti. Per spostare la posizione di una strategia di selezione (o di un gruppo di strategie) all&#39;interno della sequenza, trascinarla e rilasciarla in un&#39;altra posizione.

   ![](assets/decision-code-based-strategy-groups.png)

   >[!NOTE]
   >
   >Solo le strategie di selezione possono essere trascinate e rilasciate all&#39;interno di una sequenza. Per modificare la posizione di un elemento di decisione, è necessario rimuoverlo e aggiungerlo nuovamente utilizzando il pulsante **[!UICONTROL Aggiungi]** dopo aver aggiunto gli altri elementi che si desidera valutare in precedenza.

   È inoltre possibile **combinare** più strategie di selezione in gruppi in modo che vengano valutate insieme e non separatamente. A tale scopo, fare clic sul pulsante **`+`** in una strategia di selezione per combinarla con un&#39;altra. Puoi anche trascinare e rilasciare una strategia di selezione su un’altra per raggruppare le due strategie in un gruppo.

   >[!NOTE]
   >
   >Gli elementi decisionali non possono essere raggruppati con altri elementi o strategie di selezione.

   Le strategie multiple e il loro raggruppamento determinano la priorità delle strategie e la classificazione delle offerte idonee. The first strategy has the highest priority and the strategies combined within the same group have the same priority.

   For example, you have two collections, one in strategy A and one in strategy B. The request is for two decision items to be sent back. Let&#39;s say there are two eligible offers from strategy A and three eligible offers from strategy B.

   * If the two strategy are **not combined** or in sequential order (1 and 2), the top two eligible offers from the first strategy will be returned in the first row. If there are not two eligible offers for the first strategy, the decision engine will move on to the next strategy in sequence to find as many offers are still needed, and ultimately will return a fallback if needed.

     ![](assets/decision-code-based-consecutive-strategies.png)

   * If the two collections are **evaluated at the same time**, as there are two eligible offers from strategy A and three eligible offers from strategy B, the five offers will all be stack ranged together based on the value determined by the respective ranking methods. Two offers are requested, therefore the top two eligible offers from these five offers will be returned.

     ![](assets/decision-code-based-combined-strategies.png)

   **Example with multiple strategies**

   Now let&#39;s consider an example where you have multiple strategies divided into different groups. You defined three strategies. Strategy 1 and Strategy 2 are combined together in Group 1 and Strategy 3 is independent (Group 2). The eligible offers for each strategy and their priority (used in the ranking function evaluation) are as follows:

   * Group 1:
      * Strategy 1 - (Offer 1, Offer 2, Offer 3) - Priority 1
      * Strategy 2 - (Offer 3, Offer 4, Offer 5) - Priority 1

   * Group 2:
      * Strategy 3 - (Offer 5, Offer 6) - Priority 0

   The highest priority strategy offers is evaluated first and added to the ranked offers list.

   * **Iteration 1:**

     Strategy 1 and Strategy 2 offers are evaluated together (Offer 1, Offer 2, Offer 3, Offer 4, Offer 5). Let&#39;s say the result is:

     Offer 1 - 10
Offer 2 - 20
Offer 3 - 30 from Strategy 1, 45 from Strategy 2. The highest of both will be considered, so 45 is taken into account.
Offerta 4 - 40
Offerta 5 - 50

     Le offerte classificate sono ora le seguenti: Offerta 5, Offerta 3, Offerta 4, Offerta 2, Offerta 1.

   * **Iterazione 2:**

     Vengono valutate le offerte della Strategia 3 (Offerta 5, Offerta 6). Supponiamo che il risultato sia:

      * Offerta 5: non verrà valutata perché esiste già nel risultato precedente.
      * Offerta 6 - 60

     Le offerte classificate sono ora le seguenti: Offerta 5 , Offerta 3, Offerta 4, Offerta 2, Offerta 1, Offerta 6.

   +++

1. Quando la strategia di selezione è pronta, fai clic su **[!UICONTROL Avanti]**.

## Aggiungere offerte di fallback {#fallback}

Dopo aver selezionato gli elementi decisionali e/o le strategie di selezione, puoi aggiungere offerte di fallback da visualizzare se nessuno degli elementi o delle strategie di selezione di cui sopra è qualificato.

È possibile selezionare qualsiasi elemento dall’elenco, in cui vengono visualizzati tutti gli elementi decisionali creati nella sandbox corrente. Se non viene definita alcuna strategia di selezione, il fallback viene visualizzato all&#39;utente indipendentemente dalle date e dal vincolo di idoneità applicato all&#39;elemento selezionato<!--nor frequency capping when available - TO CLARIFY-->.

![](assets/decision-code-based-strategy-fallback.png)

>[!NOTE]
> I fallback sono facoltativi. È possibile selezionare fino al numero di elementi richiesti. Se nessuna è idonea e non è impostato alcun fallback, non viene visualizzato nulla.

## Verifica e salva la policy di decisione {#review}

Dopo aver configurato una strategia di selezione e aggiunto le offerte di fallback, fai clic su **[!UICONTROL Avanti]** per rivedere e salvare i criteri di decisione, quindi fai clic su **[!UICONTROL Crea]** per confermare la creazione dei criteri.

>[!IMPORTANT]
>
>Una volta creato un criterio decisionale, qualsiasi modifica apportata può richiedere fino a 15 minuti per propagarsi in tutte le aree di dati e fino a 30 minuti per il Canada. Ciò include modifiche quali l’aggiunta di un nuovo elemento decisionale a una raccolta, la modifica di una regola in un elemento, la modifica del contenuto di un elemento o l’aggiornamento di una formula.

Puoi modificare o eliminare un criterio di decisione in qualsiasi momento utilizzando il pulsante con i puntini di sospensione nell&#39;editor di personalizzazione o nel menu **[!UICONTROL Decisioning]** all&#39;interno del riquadro delle proprietà del componente.

>[!BEGINTABS]

>[!TAB Modifica o elimina un criterio dall&#39;editor di personalizzazione]

![](assets/decision-policy-edit.png)

>[!TAB Modificare o eliminare un criterio dal menu Decisioning]

![](assets/decision-policy-edit-properties.png)

>[!ENDTABS]

## Assegnare un posizionamento (e-mail) {#placement}

For emails, you need to define a placement for the component associated to the decision policy. To do so, click the **[!UICONTROL Decisioning]** button in the component properties pane and select **[!UICONTROL Assign placement]**. [Learn how to work with placements](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

## Passaggi successivi {#next-steps}

Now that you understand how to create a decision policy, you&#39;re ready to use it into [!DNL Journey Optimizer] channels to deliver offers.

➡️ [Scopri come utilizzare i criteri di decisione nei messaggi](../experience-decisioning/use-decision-policy.md)
