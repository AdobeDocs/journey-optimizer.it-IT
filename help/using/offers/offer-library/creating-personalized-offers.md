---
title: Creare offerte personalizzate
description: Scopri come creare offerte personalizzate in Adobe Experience Platform.
feature: Offerte
topic: Integrazioni
role: User
level: Intermediate
source-git-commit: 0e5cc9101ff382ce9fde442da38eb46aa28e9c77
workflow-type: tm+mt
source-wordcount: '916'
ht-degree: 4%

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
   >La sezione **[!UICONTROL Offer attributes]** ti consente di associare coppie di valori chiave all’offerta a scopo di reporting e analisi.

## Configurare le rappresentazioni dell’offerta {#representations}

1. Aggiungi una o più rappresentazioni per la tua offerta utilizzando il pulsante **[!UICONTROL Add representation]** .

   >[!NOTE]
   >
   >Un’offerta può essere visualizzata in posizioni diverse all’interno di un messaggio: in un banner superiore con un’immagine, come testo in un paragrafo, come blocco html, ecc. Più rappresentazioni sono disponibili, più opportunità esistono per utilizzare l’offerta in contesti di posizionamento diversi.

1. Per ogni rappresentazione, specifica il **[!UICONTROL Channel]** e il **[!UICONTROL Placement]** dove verrà visualizzata l’offerta.

   ![](../../assets/channel-placement.png)

   Il pulsante **[!UICONTROL Browse]** ti consente di filtrare i posizionamenti disponibili e filtrarli in base al canale e/o al tipo di contenuto.

   ![](../../assets/browse-placements.png)

1. Aggiungi contenuti a ogni rappresentazione proveniente dalla libreria Adobe Experience Cloud Assets o da una posizione pubblica esterna.

   * Per aggiungere contenuto dalla libreria Adobe Experience Cloud Assets, trascinalo dal riquadro di sinistra all’area di rappresentazione, quindi specifica l’URL da associare al contenuto nel campo **[!UICONTROL Destination link]** .

      >[!NOTE]
      >
      >Il contenuto può essere trascinato e rilasciato solo dal Selettore risorse nel pannello a sinistra. È disponibile per l’uso solo il contenuto corrispondente al tipo di contenuto del posizionamento.

      ![](../../assets/offer_drag_content.png)

   * Per aggiungere contenuto da una posizione pubblica esterna, fai clic sul pulsante **[!UICONTROL Add content]** , quindi specifica il nome, l’URL e il collegamento Destinazione del contenuto da aggiungere.

      Assicurati che il contenuto che stai aggiungendo corrisponda al tipo di contenuto del posizionamento selezionato.

      ![](../../assets/offer_add_content.png)

   * È inoltre possibile inserire contenuto di tipo testo. A questo scopo, fai clic sul pulsante **[!UICONTROL Add content]** , quindi seleziona l&#39;opzione **[!UICONTROL Custom text]** . Nel campo **[!UICONTROL Text]** , digita il testo che verrà visualizzato nell’offerta.

      >[!NOTE]
      >
      >Questa opzione non è disponibile per i posizionamenti di tipo immagine.

      ![](../../assets/offer_text_content.png)

## Aggiungere regole e vincoli di idoneità {#eligibility}

Le regole e i vincoli di idoneità ti consentono di definire le condizioni in cui verrà visualizzata un’offerta.

1. Configura il **[!UICONTROL Offer eligibility]**. Per impostazione predefinita, è selezionata l’opzione **[!UICONTROL All visitors]** regola decisionale , il che significa che qualsiasi profilo sarà idoneo per la presentazione dell’offerta.

   Puoi limitare la presentazione dell’offerta ai membri di uno o più segmenti di Adobe Experience Platform. A questo scopo, attiva l’opzione **[!UICONTROL Visitors who fall into one or multiple segments]** , quindi aggiungi uno o più segmenti dal riquadro a sinistra e combinali utilizzando gli operatori logici **[!UICONTROL And]** / **[!UICONTROL Or]**.

   Per ulteriori informazioni su come lavorare con i segmenti, consulta la [documentazione Servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

   ![](../../assets/offer-eligibility-segment.png)

   Se desideri associare una regola decisionale specifica all&#39;offerta, seleziona **[!UICONTROL By defined decision rule]**, quindi trascina la regola desiderata dal riquadro di sinistra nell&#39;area **[!UICONTROL Decision rule]**. Per ulteriori informazioni su come creare una regola decisionale, consulta [questa sezione](../offer-library/creating-decision-rules.md).

   ![](../../assets/offer_rule.png)

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

Una volta definite le regole di idoneità e i vincoli, viene visualizzato un riepilogo delle proprietà dell’offerta. Se tutto è configurato correttamente e l&#39;offerta è pronta per essere presentata agli utenti, fai clic su **[!UICONTROL Finish]**, quindi seleziona **[!UICONTROL Save and approve]**.

Puoi anche salvare l’offerta come bozza, per modificarla e approvarla in un secondo momento.

![](../../assets/offer_review.png)

L’offerta viene visualizzata nell’elenco con lo stato **[!UICONTROL Live]** o **[!UICONTROL Draft]** , a seconda che sia stata approvata o meno nel passaggio precedente.

È ora pronto per essere consegnato agli utenti. È possibile selezionarlo per visualizzarne le proprietà e modificarlo o eliminarlo.

![](../../assets/offer_created.png)

Una volta creata un’offerta, puoi fare clic sul suo nome nell’elenco per accedere alle informazioni dettagliate e monitorare tutte le modifiche apportate utilizzando la scheda **[!UICONTROL Change log]** (consulta [Monitoraggio delle modifiche alle offerte e alle decisioni](../get-started/user-interface.md#monitoring-changes)).

## Video tutorial {#video}

>[!NOTE]
>
>Questo video si applica al servizio di applicazione Offer Decisioning integrato in Adobe Experience Platform. Tuttavia, fornisce indicazioni generiche per utilizzare Offerta nel contesto di Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329375?quality=12)
