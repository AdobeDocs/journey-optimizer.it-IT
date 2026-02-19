---
title: Creare criteri di decisioni
description: Scopri come creare criteri di decisioni
feature: Decisioning
topic: Integrations
role: User
level: Experienced
version: Journey Orchestration
exl-id: e7a89354-28ea-431f-a15d-a8c18946d266
source-git-commit: 708c67796974e019417efbf086ab60d26dfca866
workflow-type: tm+mt
source-wordcount: '2189'
ht-degree: 5%

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

Per presentare ai clienti l’offerta e l’esperienza dinamica migliore, aggiungi un criterio di decisione al contenuto di una campagna o di un percorso, quindi configura gli elementi da restituire e la strategia di selezione da utilizzare. A questo scopo, segui i passaggi riportati qui sotto:

1. [Aggiungere un criterio di decisione](#add)
1. [Configura il criterio di decisione](#configure). Aggiungere un nome e specificare il numero di elementi da restituire per il canale e-mail.
1. [Imposta una sequenza strategica](#strategy) - Seleziona gli elementi da restituire con il criterio di decisione.
1. [Seleziona offerte di fallback](#fallback) (facoltativo): seleziona gli elementi da visualizzare se non sono stati qualificati elementi o strategie di selezione.
1. [Rivedi e salva](#review) la strategia di selezione
1. [Assegna un posizionamento](#placement) (canale e-mail)

>[!AVAILABILITY]
>
>I criteri delle decisioni sono disponibili per tutti i clienti per **Esperienza basata su codice**, **Notifica push** e canali SMS.
>
>Le decisioni per il canale E-mail sono disponibili in Disponibilità limitata. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

## Aggiungere un criterio di decisione {#add}

Per aggiungere un criterio di decisione al messaggio, apri un percorso o una campagna e seleziona un&#39;[azione canale](../building-journeys/journeys-message.md).

Modifica il contenuto del messaggio e sfoglia le schede seguenti per ulteriori informazioni su come aggiungere il criterio di decisione in base al canale selezionato.

>[!BEGINTABS]

>[!TAB Esperienza basata su codice]

Per le esperienze basate su codice, puoi aggiungere un nuovo criterio di decisione utilizzando l&#39;**editor di codice** o il menu **Decisioning** disponibile nel riquadro delle proprietà.

+++Aggiungere un criterio di decisione dall’editor di codice

1. Apri l&#39;editor di codice utilizzando il pulsante **[!UICONTROL Modifica codice]**.

1. Passa al menu **[!UICONTROL Criteri di decisione]**, quindi fai clic sul pulsante **[!UICONTROL Aggiungi criterio di decisione]**.

   ![](assets/decision-policy-add-code-editor.png)

+++

+++Aggiungere un criterio di decisione dal menu Decisioning

1. Fare clic sull&#39;icona ![](assets/do-no-localize/decisioning-icon.png) nel riquadro delle proprietà per accedere al menu **[!UICONTROL Decisioning]**.

1. Fare clic sul pulsante **[!UICONTROL Aggiungi criterio di decisione]**.

   ![](assets/decision-policy-add-code.png)

+++

>[!TAB E-mail]

1. Attiva/disattiva l&#39;opzione **[!UICONTROL Abilita decisioning]**.

   ![](assets/decision-policy-enable.png)

   >[!IMPORTANT]
   >
   >L’abilitazione del decisioning cancella il contenuto delle e-mail esistenti. Se hai già progettato l’e-mail, assicurati di salvare preventivamente il contenuto come modello.

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
>Experience Decisioning con notifiche push richiede una versione specifica del SDK mobile. Prima di implementare questa funzione, controlla le [note sulla versione](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} per identificare la versione richiesta e assicurarti di aver effettuato l&#39;aggiornamento di conseguenza. Puoi anche visualizzare tutte le versioni di SDK disponibili per la tua piattaforma in [questa sezione](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.

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

   Le strategie multiple e il loro raggruppamento determinano la priorità delle strategie e la classificazione delle offerte idonee. La prima strategia ha la massima priorità e le strategie combinate all&#39;interno dello stesso gruppo hanno la stessa priorità.

   Ad esempio, sono disponibili due raccolte, una nella strategia A e una nella strategia B. La richiesta prevede il rinvio di due elementi decisionali. Supponiamo che vi siano due offerte ammissibili dalla strategia A e tre offerte ammissibili dalla strategia B.

   * Se le due strategie sono **non combinate** o in ordine sequenziale (1 e 2), le prime due offerte idonee della prima strategia verranno restituite nella prima riga. Se non ci sono due offerte idonee per la prima strategia, il motore decisionale passerà alla strategia successiva in sequenza per trovare quante offerte sono ancora necessarie e alla fine restituirà un fallback, se necessario.

     ![](assets/decision-code-based-consecutive-strategies.png)

   * Se le due raccolte sono **valutate contemporaneamente**, poiché esistono due offerte idonee dalla strategia A e tre offerte idonee dalla strategia B, le cinque offerte saranno tutte raggruppate in base al valore determinato dai rispettivi metodi di classificazione. Sono richieste due offerte, pertanto verranno restituite le prime due offerte idonee di queste cinque.

     ![](assets/decision-code-based-combined-strategies.png)

   **Esempio con più strategie**

   Prendiamo ora in considerazione un esempio in cui si dispone di più strategie suddivise in gruppi diversi. Hai definito tre strategie. La strategia 1 e la strategia 2 sono combinate nel gruppo 1 e la strategia 3 è indipendente (gruppo 2). Le offerte ammissibili per ciascuna strategia e la loro priorità (utilizzata nella valutazione della funzione di classificazione) sono le seguenti:

   * Gruppo 1:
      * Strategia 1 - (offerta 1, offerta 2, offerta 3) - Priorità 1
      * Strategia 2 - (offerta 3, offerta 4, offerta 5) - Priorità 1

   * Gruppo 2:
      * Strategia 3 - (Offerta 5, Offerta 6) - Priorità 0

   Le offerte di strategia con priorità più alta vengono valutate per prime e aggiunte all’elenco delle offerte classificate.

   * **Iterazione 1:**

     Le offerte di Strategia 1 e Strategia 2 vengono valutate insieme (Offerta 1, Offerta 2, Offerta 3, Offerta 4, Offerta 5). Supponiamo che il risultato sia:

     Offerta 1 - 10
Offerta 2 - 20
Offerta 3-30 dalla Strategia 1, 45 dalla Strategia 2. Il più alto di entrambi sarà considerato, quindi 45 è preso in considerazione.
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

Per le e-mail, devi definire un posizionamento per il componente associato al criterio decisionale. A tale scopo, fare clic sul pulsante **[!UICONTROL Decisioning]** nel riquadro delle proprietà del componente e selezionare **[!UICONTROL Assegna posizionamento]**. [Scopri come utilizzare i posizionamenti](../experience-decisioning/placements.md)

![](assets/decision-policy-rail.png)

## Passaggi successivi {#next-steps}

Ora che sai come creare un criterio di decisione, puoi utilizzarlo in [!DNL Journey Optimizer] canali per distribuire le offerte.

➡️ [Scopri come utilizzare i criteri di decisione nei messaggi](../experience-decisioning/use-decision-policy.md)
