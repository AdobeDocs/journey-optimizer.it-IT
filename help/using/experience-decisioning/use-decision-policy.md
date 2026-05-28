---
title: Utilizzare i criteri di decisione nei messaggi
description: Scopri come utilizzare i criteri di decisione nei messaggi.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
version: Journey Orchestration
exl-id: 35fc3cf2-1b91-4f30-ad71-f9d7d2a0291c
TQID: https://experienceleague.adobe.com/zKV67LEfRVmEk9Fac-D45qdHLqbuVCS3rUt6Rt0HB7w
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: e0eb8757-182f-49f3-94a4-1587d16f5094id: e1e0219c-f879-479f-8427-888ed2a6e9c2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: b94f1c1a557a6c47d3eb81f3660b09b1fde59f5a
workflow-type: tm+mt
source-wordcount: 1164
ht-degree: 2%

---

# Utilizzare i criteri di decisione nei messaggi {#create-decision}

Dopo aver aggiunto al contenuto un criterio di decisione, puoi utilizzare per la personalizzazione gli attributi degli elementi di decisione restituiti. A tal fine, inserisci innanzitutto il codice del criterio di decisione nel contenuto.

>[!CAUTION]
>
>I criteri delle decisioni sono disponibili per tutti i clienti per i canali **Esperienza basata su codice**, **SMS**, **Notifica push** e **E-mail**.

## Inserire il codice del criterio di decisione {#insert}

>[!BEGINTABS]

>[!TAB Esperienza basata su codice]

1. Modifica l&#39;esperienza basata su codice e passa a **[!UICONTROL Criterio decisionale]**.

2. Selezionare **[!UICONTROL Inserisci criterio]** per aggiungere il codice del criterio di decisione.

   ![](assets/decision-code-based-add-decision.png)

>[!NOTE]
>
>Per le esperienze basate su codice, se il criterio di decisione contiene elementi di decisione, compresi i frammenti, puoi sfruttarli nel codice del criterio di decisione. [Scopri come sfruttare i frammenti](fragments-decision-policies.md)

>[!TAB E-mail]

1. Apri **Personalization Editor** e passa a **[!UICONTROL Criteri di decisione]**.

2. Seleziona **[!UICONTROL Inserisci sintassi]** per aggiungere il codice per il criterio decisionale.

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >Se l’opzione di inserimento non viene visualizzata, è possibile che per il componente principale sia già configurato un criterio di decisione.

3. Se al componente non è ancora stato assegnato alcun posizionamento, selezionarne uno dall&#39;elenco e fare clic su **[!UICONTROL Assegna]**.

   ![](assets/decision-policy-placement.png)

   >[!NOTE]
   >
   >Se utilizzi più criteri di decisione nella stessa e-mail (ad esempio, uno per l’intestazione e uno per il piè di pagina), la stessa offerta viene deduplicata tra i posizionamenti: non viene sottoposta a rendering due volte. Il secondo criterio di decisione non restituirà alcun contenuto e visualizzerà uno spazio vuoto, a meno che non sia stata configurata un’offerta di fallback, nel qual caso verrà visualizzato il fallback.

Puoi anche inserire il codice del criterio di decisione quando utilizzi la modalità **[!UICONTROL Crea il codice]** in E-mail Designer. Passa a **[!UICONTROL Criteri di decisione]** e seleziona **[!UICONTROL Sintassi di inserimento]**. Verrà visualizzata l&#39;interfaccia utente per la selezione del posizionamento in modo da poter assegnare direttamente un posizionamento. [Scopri come programmare il contenuto delle e-mail](../email/code-content.md).

>[!AVAILABILITY]
>
>L&#39;inserimento dei criteri di decisione in **[!UICONTROL Crea un codice per la tua modalità]** è in disponibilità limitata.

>[!NOTE]
>
>In modalità **[!UICONTROL Crea codice personalizzato]**, è possibile restituire un solo elemento di decisione per criterio, perché il componente **[!UICONTROL Ripeti griglia]** non è disponibile.

>[!TAB SMS]

1. Apri **Personalization Editor** e passa a **[!UICONTROL Criteri di decisione]**.

2. Seleziona **[!UICONTROL Inserisci sintassi]** per aggiungere il codice per il criterio decisionale.

   ![](assets/decision-policy-add-sms-insert-syntax.png)

>[!TAB Invia]

1. Apri **Personalization Editor** e passa a **[!UICONTROL Criteri di decisione]**.

2. Seleziona **[!UICONTROL Inserisci sintassi]** per aggiungere il codice per il criterio decisionale.

   ![](assets/decision-policy-add-push-insert-syntax.png)

>[!IMPORTANT]
>
>Experience Decisioning con notifiche push richiede una versione specifica del SDK mobile. Prima di implementare questa funzione, controlla le [note sulla versione](https://developer.adobe.com/client-sdks/home/release-notes){target="_blank"} per identificare la versione richiesta e assicurarti di aver effettuato l&#39;aggiornamento di conseguenza. Puoi anche visualizzare tutte le versioni di SDK disponibili per la tua piattaforma in [questa sezione](https://developer.adobe.com/client-sdks/home/current-sdk-versions){target="_blank"}.

>[!ENDTABS]

Viene aggiunto il codice del criterio di decisione. Ora puoi utilizzare gli attributi degli elementi decisionali restituiti per personalizzare il contenuto.

>[!NOTE]
>
>Per l’esperienza basata su codice e i canali e-mail, ripeti questa sequenza una volta per ogni elemento decisionale che desideri restituire. Ad esempio, se hai scelto di restituire 2 elementi durante la [creazione della decisione](create-decision-policy.md), ripeti la sequenza due volte. Per i canali SMS e Push, è possibile restituire un solo elemento decisionale.

## Personalizzare con gli attributi degli elementi di decisione {#attributes}

Dopo aver aggiunto il codice per un criterio di decisione nel contenuto, tutti gli attributi degli elementi di decisione restituiti diventano disponibili per la personalizzazione. [Scopri come utilizzare la personalizzazione](../personalization/personalize.md).

Gli attributi sono archiviati nello schema [catalogo](catalogs.md) delle &quot;Offerte&quot;. Vengono visualizzati nelle seguenti cartelle dell’editor di personalizzazione:
* **Attributi personalizzati**: cartella `_\<imsOrg\>`
* **Attributi standard**: cartella `_experience`

Gli attributi degli elementi decisionali e gli attributi contestuali non sono supportati per impostazione predefinita nei frammenti [!DNL Journey Optimizer]. Tuttavia, puoi utilizzare in alternativa le variabili globali, come descritto di seguito.

![](assets/decision-code-based-decision-attributes.png)

Per aggiungere un attributo, fare clic sull&#39;icona **`+`** accanto all&#39;attributo. Puoi aggiungere tutti gli attributi necessari. Puoi anche includere altri attributi di personalizzazione, ad esempio i dati del profilo.

* Per i canali **Email** e **Code-based**, racchiudi gli attributi nel loop `#each` tra parentesi quadre `[ ]` e aggiungi una virgola prima del tag `/each` di chiusura.

  +++Vedi esempio

  ![](assets/decision-code-based-wrap-code.png)

  +++

* Per i canali **SMS** e **Push**, accertati di inserire gli attributi dopo il codice di sintassi per il criterio di decisione. Questa sintassi deve essere sempre mantenuta alla riga 1.

  +++Vedi esempio

  ![](assets/decision-added-sms.png)

  +++

  >[!NOTE]
  >Se inserisci un attributo di risorsa immagine nel contenuto SMS o Push (ad esempio, nel titolo o nel corpo), il valore dell’attributo viene visualizzato come URL. L’immagine stessa non viene rappresentata in questi campi.

* Per abilitare il tracciamento dell&#39;elemento di decisione, aggiungere l&#39;attributo `trackingToken`: `trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

## Anteprima e test del contenuto

Dopo aver generato il contenuto, visualizzalo in anteprima e testalo prima di attivare il percorso o la campagna. Gli elementi decisionali eseguono il rendering in base ai profili selezionati nell’interfaccia di simulazione. [Scopri come visualizzare in anteprima e verificare il contenuto](../content-management/preview-test.md).

## Passaggi successivi {#final-steps}

Una volta che il contenuto è pronto, rivedi e pubblica la campagna o il percorso:

* [Pubblicare un percorso](../building-journeys/publish-journey.md)
* [Rivedere e attivare una campagna](../campaigns/review-activate-campaign.md)

Per le esperienze basate su codice, non appena lo sviluppatore effettua una chiamata API o SDK per recuperare il contenuto per la superficie definita nella configurazione del canale, le modifiche verranno applicate alla pagina web o all’app.

## Visualizza i dettagli dei criteri di decisione dal riepilogo della campagna {#decision-policy-summary}

Quando una [campagna](../campaigns/get-started-with-campaigns.md) attivata da un&#39;azione o da un&#39;API utilizza i criteri di decisione nel contenuto, nella pagina di riepilogo della campagna viene visualizzata una sezione **[!UICONTROL Criteri di decisione]** in cui sono elencati tutti i criteri utilizzati nella campagna.

Puoi anche accedere ai dettagli tecnici di ogni criterio decisionale e copiarli negli Appunti, il che può essere utile per risolvere i problemi con il supporto Adobe o il tuo team di progettazione.

+++ Per accedere ai dettagli dei criteri di decisione e alle informazioni tecniche, segui i passaggi riportati di seguito.

1. Apri il riepilogo della campagna facendo clic su **[!UICONTROL Rivedi per attivare]** durante [configurazione](../campaigns/review-activate-campaign.md#action-campaign-review) oppure aprendo una campagna dall&#39;elenco **[!UICONTROL Campagne]**.

1. Nella sezione **[!UICONTROL Criteri di decisione]** sono elencati tutti i criteri utilizzati nella campagna.

   ![](assets/campaign-summary-decision-policies.png)

1. Selezionare un criterio di decisione o fare clic su **[!UICONTROL Visualizza tutto]**. Puoi rivedere i dettagli di ogni policy, tra cui:

   * Strategie utilizzate nel criterio decisionale
   * Numero di elementi da restituire
   * La raccolta, il metodo di classificazione e le regole di idoneità utilizzati per ogni strategia di selezione
   * Offerta di fallback utilizzata se nessun elemento di decisione è idoneo

   ![](assets/campaign-decision-policy-details.png)

1. Fai clic su una raccolta per visualizzare tutti gli elementi decisionali in essa contenuti.

1. Fai clic su un elemento decisionale per accedere ai relativi dettagli e modificarlo, se necessario; si apre in una nuova scheda del browser. In alternativa, fare clic su **[!UICONTROL Visualizza elemento]** per visualizzare gli elementi decisionali non inclusi in una raccolta.

   ![](assets/campaign-decision-policy-collection.png)

1. È inoltre possibile visualizzare informazioni sui metodi di classificazione e sulle regole di idoneità utilizzati per ciascuna strategia di selezione.

   ![](assets/campaign-decision-policy-eligibility.png){width="80%"}

1. Nel riepilogo della campagna, puoi anche selezionare un criterio di decisione dalla sezione **[!UICONTROL Azioni]** e fare clic sull&#39;icona **Informazioni** per accedere ai dettagli tecnici del criterio di decisione.

   ![](assets/campaign-decision-policy-information.png)

1. Fai clic sull&#39;icona **Copia negli Appunti** per copiare negli Appunti una rappresentazione JSON dei criteri di decisione.

   Il JSON copiato include il nome e l’ID dell’organizzazione, il nome della sandbox, l’ID del criterio di decisione e la struttura completa del criterio di decisione. Puoi condividere queste informazioni con il supporto Adobe o con il team di progettazione per risolvere più rapidamente i problemi relativi ai criteri decisionali.

+++

## Utilizzare le dashboard di reporting

Per visualizzare le prestazioni delle decisioni, puoi visualizzare le metriche di decisione predefinite nel rapporto della campagna o del percorso, oppure puoi creare dashboard di Customer Journey Analytics personalizzati per misurare le prestazioni e ottenere informazioni approfondite sul modo in cui i criteri decisionali e le offerte vengono consegnati e utilizzati. [Ulteriori informazioni sul reporting di Decisioning](cja-reporting.md).

![](../reports/assets/cja-decisioning-item-performance.png)