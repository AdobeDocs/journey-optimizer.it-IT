---
title: Creare offerte personalizzate
description: Scopri come creare offerte personalizzate in Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 4a53ea96-632a-41c7-ab15-b85b99db4f3e
source-git-commit: 41f43f6e702dbadfcd28d14154895a65ec15ed65
workflow-type: tm+mt
source-wordcount: '1319'
ht-degree: 3%

---

# Creare offerte personalizzate {#creating-personalized-offers}

Prima di creare un’offerta, accertati di aver creato:

* Un **posizionamento** in cui verrà visualizzata l&#39;offerta. Consulta [Creare posizionamenti](../offer-library/creating-placements.md)
* Una **regola decisionale** che definirà la condizione in cui verrà presentata l&#39;offerta. Consulta [Creare regole decisionali](../offer-library/creating-decision-rules.md).
* Uno o più **tag** da associare all&#39;offerta. Consulta [Creare tag](../offer-library/creating-tags.md).

➡️ [Scopri questa funzione nel video](#video)

L’elenco delle offerte personalizzate è accessibile nel menu **[!UICONTROL Offers]** .

![](../../assets/offers_list.png)

## Creare l’offerta {#create-offer}

Per creare un’ **offerta**, effettua le seguenti operazioni:

1. Fare clic su **[!UICONTROL Create offer]**, quindi selezionare **[!UICONTROL Personalized offer]**.

   ![](../../assets/create_offer.png)

1. Specifica il nome dell’offerta, la data e l’ora di inizio e fine dell’offerta. Puoi anche associare uno o più tag esistenti all’offerta, per facilitarne la ricerca e l’organizzazione.

   ![](../../assets/offer_details.png)

   >[!NOTE]
   >
   >La sezione **[!UICONTROL Offer attributes]** ti consente di associare coppie chiave-valore all’offerta a scopo di reporting e analisi.

## Configurare le rappresentazioni dell’offerta {#representations}

Un’offerta può essere visualizzata in posizioni diverse all’interno di un messaggio: in un banner superiore con un’immagine, come testo in un paragrafo, come blocco HTML, ecc. Più rappresentazioni sono disponibili, più opportunità esistono per utilizzare l’offerta in contesti di posizionamento diversi.

Per aggiungere una o più rappresentazioni all’offerta e configurarle, effettua le seguenti operazioni.

1. Per la prima rappresentazione, inizia selezionando la **[!UICONTROL Channel]** che verrà utilizzata.

   ![](../../assets/channel-placement.png)

   >[!NOTE]
   >
   >Nell’elenco a discesa **[!UICONTROL Placement]** vengono visualizzati solo i posizionamenti disponibili per il canale selezionato.


1. Seleziona un posizionamento dall’elenco.

   Puoi inoltre utilizzare il pulsante accanto all’elenco a discesa **[!UICONTROL Placement]** per sfogliare tutti i posizionamenti.

   ![](../../assets/browse-button-placements.png)

   È comunque possibile filtrare i posizionamenti in base al relativo canale e/o tipo di contenuto. Scegli un posizionamento e fai clic su **[!UICONTROL Select]**.

   ![](../../assets/browse-placements.png)

1. Aggiungi contenuto alla tua rappresentazione. Scopri come in [questa sezione](#content).

1. Quando aggiungi contenuto, ad esempio un&#39;immagine o un URL, puoi specificare un **[!UICONTROL Destination link]**: gli utenti che fanno clic sull’offerta verranno indirizzati alla pagina corrispondente.

   ![](../../assets/offer-destination-link.png)

1. Infine, seleziona la lingua scelta per identificare e gestire gli elementi da visualizzare agli utenti.

1. Per aggiungere un’altra rappresentazione, utilizza il pulsante **[!UICONTROL Add representation]** e aggiungi tutte le rappresentazioni necessarie.

   ![](../../assets/offer-add-representation.png)

1. Dopo aver aggiunto tutte le rappresentazioni, seleziona **[!UICONTROL Next]**.

## Definire il contenuto per le rappresentazioni {#content}

È possibile aggiungere diversi tipi di contenuto a una rappresentazione.

>[!NOTE]
>
>È disponibile per l’uso solo il contenuto corrispondente al tipo di contenuto del posizionamento.

### Aggiungere immagini

Se il posizionamento selezionato è di tipo immagine, puoi aggiungere contenuto proveniente dalla libreria **Adobe Experience Cloud Asset**, un archivio centralizzato di risorse fornito da [!DNL Adobe Experience Manager Assets Essentials].

>[!NOTE]
>
> Per lavorare con [Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=en){target=&quot;_blank&quot;}, devi distribuire [!DNL Assets Essentials] per la tua organizzazione e assicurarti che gli utenti facciano parte dei profili di prodotto **Assets Essentials Consumer Users** o/and **Assets Essentials Users**. Ulteriori informazioni su [questa pagina](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

1. Scegli l’opzione **[!UICONTROL Asset library]**.

1. Seleziona **[!UICONTROL Browse]**.

   ![](../../assets/offer-browse-asset-library.png)

1. Sfoglia le risorse per selezionare l&#39;immagine desiderata

1. Fai clic su **[!UICONTROL Select]**.

   ![](../../assets/offer-select-asset.png)

### Aggiungi URL

Per aggiungere contenuto da una posizione pubblica esterna, seleziona **[!UICONTROL URL]**, quindi immetti l’indirizzo URL del contenuto da aggiungere.

![](../../assets/offer-content-url.png)

### Aggiungi testo personalizzato {#custom-text}

È inoltre possibile inserire contenuto di tipo testo quando si seleziona una posizione compatibile.

1. Seleziona l&#39;opzione **[!UICONTROL Custom]**.

   >[!NOTE]
   >
   >Questa opzione non è disponibile per i posizionamenti di tipo immagine.

1. Digita il testo che verrà visualizzato nell’offerta nell’area dedicata.

   ![](../../assets/offer-text-content2.png)

## Aggiungere regole e vincoli di idoneità {#eligibility}

Le regole di idoneità e i vincoli ti consentono di definire le condizioni in cui verrà visualizzata un’offerta.

1. Configura il **[!UICONTROL Offer eligibility]**.

   * Per impostazione predefinita, è selezionata l’opzione **[!UICONTROL All visitors]** regola decisionale , il che significa che qualsiasi profilo sarà idoneo per la presentazione dell’offerta.

   * Puoi limitare la presentazione dell’offerta ai membri di uno o più segmenti di Adobe Experience Platform. A questo scopo, attiva l’opzione **[!UICONTROL Visitors who fall into one or multiple segments]** , quindi aggiungi uno o più segmenti dal riquadro a sinistra e combinali utilizzando gli operatori logici **[!UICONTROL And]** / **[!UICONTROL Or]**.

      Per ulteriori informazioni su come lavorare con i segmenti, consulta [questa pagina](../../segment/about-segments.md).

      ![](../../assets/offer-eligibility-segment.png)

   * Se desideri associare una regola decisionale specifica all&#39;offerta, seleziona **[!UICONTROL By defined decision rule]**, quindi trascina la regola desiderata dal riquadro di sinistra nell&#39;area **[!UICONTROL Decision rule]**. Per ulteriori informazioni su come creare una regola decisionale, consulta [questa sezione](../offer-library/creating-decision-rules.md).

      ![](../../assets/offer_rule.png)

      >[!CAUTION]
      >
      >Le offerte basate su eventi non sono attualmente supportate in [!DNL Journey Optimizer]. Se crei una regola decisionale basata su un [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target=&quot;_blank&quot;}, non potrai sfruttarla in un&#39;offerta.
   Ulteriori informazioni sull&#39;utilizzo dei segmenti rispetto alle regole decisionali in [questa sezione](../offer-activities/create-offer-activities.md#segments-vs-decision-rules).

1. Definisci la **[!UICONTROL Priority]** dell’offerta rispetto alle altre se l’utente è idoneo per più di un’offerta. Maggiore sarà la priorità di un&#39;offerta, maggiore sarà la sua priorità rispetto ad altre offerte.

1. Specifica l’ **[!UICONTROL Capping]** dell’offerta, ovvero il numero di volte in cui l’offerta verrà presentata in totale per tutti gli utenti. Se l’offerta è stata consegnata a tutti gli utenti per il numero di volte specificato in questo campo, la relativa consegna verrà interrotta.

   >[!NOTE]
   >
   >Il numero di volte in cui viene proposta un’offerta viene calcolato al momento della preparazione dell’e-mail. Ad esempio, se prepari un’e-mail contenente una serie di offerte, questi numeri vengono conteggiati in base al tetto massimo, indipendentemente dal fatto che l’e-mail venga inviata o meno.
   >
   >Se una consegna e-mail viene eliminata o se la preparazione viene eseguita nuovamente prima dell’invio, il valore di limite per l’offerta viene aggiornato automaticamente.

   ![](../../assets/offer_capping.png)

   Nell’esempio precedente:

   * La priorità dell&#39;offerta è impostata su &quot;50&quot;, il che significa che l&#39;offerta sarà presentata prima delle offerte con una priorità compresa tra 1 e 49 e dopo quelle con una priorità di almeno 51.
   * L’offerta verrà considerata solo per gli utenti che corrispondono alla regola di decisione &quot;Clienti Gold Loyalty&quot;.
   * L’offerta viene presentata una sola volta per utente.

## Rivedi l’offerta {#review}

Una volta definite le regole di idoneità e i vincoli, viene visualizzato un riepilogo delle proprietà dell’offerta.

1. Assicurati che tutto sia configurato correttamente.

1. Quando l’offerta è pronta per essere presentata agli utenti, fai clic su **[!UICONTROL Finish]**.

1. Seleziona **[!UICONTROL Save and approve]**.

   ![](../../assets/offer_review.png)

   Puoi anche salvare l’offerta come bozza, per modificarla e approvarla in un secondo momento.

L’offerta viene visualizzata nell’elenco con lo stato **[!UICONTROL Approved]** o **[!UICONTROL Draft]** , a seconda che sia stata approvata o meno nel passaggio precedente.

È ora pronto per essere consegnato agli utenti.

![](../../assets/offer_created.png)

## Elenco delle offerte {#offer-list}

Dall’elenco delle offerte, puoi selezionare l’offerta per visualizzarne le proprietà. Puoi anche modificarlo, modificarne lo stato (**Bozza**, **Approvato**, **Archiviato**), duplicare l’offerta o eliminarla.

![](../../assets/offer_created.png)

Seleziona il pulsante **[!UICONTROL Edit]** per tornare alla modalità di modifica dell&#39;offerta, dove puoi modificare i [dettagli](#create-offer), [rappresentazioni](#representations) dell&#39;offerta, nonché le [regole e vincoli di idoneità](#eligibility).

Seleziona un’offerta approvata e fai clic su **[!UICONTROL Undo approve]** per impostare nuovamente lo stato dell’offerta su **[!UICONTROL Draft]**.

Per impostare nuovamente lo stato su **[!UICONTROL Approved]**, selezionare il pulsante corrispondente visualizzato.

![](../../assets/offer_approve.png)

Il pulsante **[!UICONTROL More actions]** abilita le azioni descritte di seguito.

![](../../assets/offer_more-actions.png)

* **[!UICONTROL Duplicate]**: crea un’offerta con le stesse proprietà, rappresentazioni, regole di idoneità e vincoli. Per impostazione predefinita, la nuova offerta ha lo stato **[!UICONTROL Draft]** .
* **[!UICONTROL Delete]**: rimuove l’offerta dall’elenco.

   >[!CAUTION]
   >
   >L’offerta e il relativo contenuto non saranno più accessibili. Questa azione non può essere annullata.
   >
   >Se l&#39;offerta viene utilizzata in una raccolta o in una decisione, non può essere eliminata. È innanzitutto necessario rimuovere l’offerta da qualsiasi oggetto.

* **[!UICONTROL Archive]**: imposta lo stato dell’offerta su  **[!UICONTROL Archived]**. L’offerta è ancora disponibile dall’elenco, ma non è possibile ripristinarne lo stato su **[!UICONTROL Draft]** o **[!UICONTROL Approved]**. È possibile duplicarla o eliminarla.

Puoi anche eliminare o modificare lo stato di più offerte contemporaneamente selezionando le caselle di controllo corrispondenti.

![](../../assets/offer_multiple-selection.png)

Se desideri modificare lo stato di diverse offerte con stati diversi, verranno modificati solo gli stati pertinenti.

![](../../assets/offer_change-status.png)

Una volta creata un’offerta, puoi fare clic sul suo nome dall’elenco.

![](../../assets/offer_click-name.png)

Ciò ti consente di accedere a informazioni dettagliate per quell’offerta. Seleziona la scheda **[!UICONTROL Change log]** per [monitorare tutte le modifiche](../get-started/user-interface.md#monitoring-changes) apportate all’offerta.

![](../../assets/offer_information.png)

## Video tutorial {#video}

>[!NOTE]
>
>Questo video si applica al servizio di applicazione Offer Decisioning integrato in Adobe Experience Platform. Tuttavia, fornisce indicazioni generiche per utilizzare Offerta nel contesto di Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
