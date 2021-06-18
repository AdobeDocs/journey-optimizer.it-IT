---
title: Creare decisioni
description: Scopri come creare le decisioni
feature: Offerte
topic: Integrazioni
role: User
level: Intermediate
source-git-commit: 21476691c6e5c5a2f8c5e36a494206fc9779c9d2
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 4%

---

# Creare decisioni {#create-offer-activities}

Le decisioni (precedentemente note come attività di offerta) sono contenitori per le offerte che sfrutteranno il modulo di decisione dell’offerta per scegliere l’offerta migliore da consegnare, a seconda del target della consegna.

![](../../assets/do-not-localize/how-to-video.png) [Scopri questa funzione nel video](#video)

L’elenco delle decisioni è accessibile nel menu **[!UICONTROL Offers]** / **[!UICONTROL Decisions]** scheda . Sono disponibili filtri per aiutarti a recuperare le decisioni in base al loro stato o alle date di inizio e fine.

![](../../assets/activities-list.png)

Prima di creare una decisione, accertati che i componenti seguenti siano stati creati nella Libreria offerte:

* [Posizionamenti](../offer-library/creating-placements.md)
* [Raccolte](../offer-library/creating-collections.md)
* [Offerte personalizzate](../offer-library/creating-personalized-offers.md)
* [Offerte di fallback](../offer-library/creating-fallback-offers.md)

## Crea la decisione {#create-activity}

1. Accedi all&#39;elenco delle decisioni, quindi fai clic su **[!UICONTROL Create activity]**.

1. Specifica il nome della decisione, la data e l&#39;ora di inizio e fine, quindi fai clic su **[!UICONTROL Next]**.

   ![](../../assets/activities-name.png)

## Aggiungere offerte {#add-offers}

1. Trascina e rilascia un posizionamento dall’elenco per aggiungerlo alla decisione, quindi fai clic su **[!UICONTROL Add collection]**.

   ![](../../assets/activities-placement.png)

1. Seleziona la raccolta contenente le offerte da considerare, quindi fai clic su **[!UICONTROL Add]**.

   ![](../../assets/activities-collection.png)

1. Le offerte selezionate vengono aggiunte al posizionamento. In questo esempio, abbiamo selezionato due offerte che verranno visualizzate in un posizionamento di tipo JSON per presentare le offerte in una soluzione di call center.

   ![](../../assets/offers-added.png)

1. Per impostazione predefinita, se più offerte sono idonee per questo posizionamento, verranno consegnate al cliente le offerte con il punteggio di priorità più alto.

   Se desideri utilizzare una formula specifica per scegliere l&#39;offerta idonea da consegnare, seleziona una formula di classificazione dall&#39;elenco a discesa **[!UICONTROL Rank offers by]**. Per ulteriori informazioni al riguardo, consulta [questa sezione](../offer-activities/configure-offer-selection.md).

1. Il campo **[!UICONTROL Constraint]** limita la selezione delle offerte per questo posizionamento. Questo vincolo può essere applicato utilizzando una regola decisionale o uno o più segmenti di Adobe Experience Platform.

   Per limitare la selezione delle offerte ai membri di un segmento Adobe Experience Platform, seleziona **[!UICONTROL Segments]**, quindi fai clic su **[!UICONTROL Add segments]**.

   ![](../../assets/activity_constraint_segment.png)

   Aggiungi uno o più segmenti dal riquadro a sinistra, combinali utilizzando gli operatori logici **[!UICONTROL And]** / **[!UICONTROL Or]**, quindi fai clic su **[!UICONTROL Select]** per confermare.

   Per ulteriori informazioni su come lavorare con i segmenti, consulta la [documentazione Servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

   ![](../../assets/activity_constraint_segment2.png)

   Se desideri aggiungere un vincolo di selezione per questo posizionamento utilizzando una regola di decisione, seleziona l’opzione **[!UICONTROL Decision rule]** , quindi trascina la regola desiderata dal riquadro di sinistra nell’area **[!UICONTROL Decision rule]**. Per ulteriori informazioni su come creare una regola decisionale, consulta [questa sezione](../offer-library/creating-decision-rules.md).

   ![](../../assets/activity_constraint_rule.png)

## Aggiungere un’offerta di fallback {#add-fallback}

Seleziona l’offerta di fallback che verrà presentata come ultima risorsa ai clienti che non soddisfano le regole e i vincoli di idoneità delle offerte, quindi fai clic su **[!UICONTROL Next]**.

![](../../assets/add-fallback-offer.png)

## Rivedi e salva la decisione {#review}

Se tutto è configurato correttamente e la tua decisione è pronta per essere utilizzata per presentare offerte ai clienti, fai clic su **[!UICONTROL Finish]**, quindi seleziona **[!UICONTROL Save and activate]**.

Puoi anche salvare la decisione come bozza, per modificarla e attivarla in un secondo momento.

![](../../assets/save-activities.png)

La decisione viene visualizzata nell’elenco con lo stato **[!UICONTROL Live]** o **[!UICONTROL Draft]** , a seconda che sia stata attivata o meno nel passaggio precedente.

È ora pronto per essere utilizzato per fornire offerte ai clienti. È possibile selezionarlo per visualizzarne le proprietà e modificarlo o eliminarlo.

Per ulteriori informazioni sulla consegna delle offerte, consulta queste sezioni:

* [Aggiungere offerte personalizzate nei messaggi](../../deliver-personalized-offers.md)
* [Consegnare offerte tramite API](../api-reference/decisions-api/deliver-offers.md)

![](../../assets/activities-created.png)

>[!NOTE]
>
>Una volta creata una decisione, puoi fare clic sul suo nome nell&#39;elenco per accedere alle informazioni dettagliate e visualizzare tutte le modifiche apportate utilizzando la scheda **[!UICONTROL Change log]** (consulta [Offerte e modifiche alle decisioni log](../get-started/user-interface.md#changes-log)).

## Video tutorial {#video}

>[!NOTE]
>
>Questo video si applica al servizio di applicazione Offer Decisioning integrato in Adobe Experience Platform. Tuttavia, fornisce indicazioni generiche per utilizzare Offerta nel contesto di Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
