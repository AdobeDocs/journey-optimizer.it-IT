---
title: Creare simulazioni
description: Scopri come creare simulazioni
feature: Offers
topic: Integrations
role: User
level: Intermediate
source-git-commit: 899b8b47d6c6121c19e485376de368358049c05f
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# Creare simulazioni

## Informazioni sulla simulazione

Per convalidare la logica decisionale, puoi simulare quali offerte verranno consegnate a un profilo di test per un determinato posizionamento.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Questo ti consente di testare e perfezionare diverse versioni delle offerte senza alcun impatto sui destinatari interessati.

>[!NOTE]
>
>Questa funzionalità simula una singola richiesta al [!DNL Decisions] API. Ulteriori informazioni su [Consegnare offerte tramite l’API Decisioni](../api-reference/decisions-api/deliver-offers.md).

Per accedere a questa funzione, seleziona la **[!UICONTROL Simulation]** dalla scheda **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** menu.

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## Selezionare i profili di test

Innanzitutto devi selezionare i profili di test che utilizzerai per la simulazione.

1. Fai clic su **[!UICONTROL Manage profile]**.

   ![](../../assets/offers_simulation-manage-profile.png)

1. Seleziona lo spazio dei nomi di identità da utilizzare per identificare i profili di test. In questo esempio, utilizzeremo il **E-mail** spazio dei nomi.

   >[!NOTE]
   >
   >Uno spazio dei nomi di identità definisce il contesto di un identificatore, ad esempio un indirizzo e-mail o un ID CRM. Ulteriori informazioni sui namespace delle identità Adobe Experience Platform [in questa sezione](../../get-started-identity.md){target=&quot;_blank&quot;}.

1. Immetti il valore dell&#39;identità e fai clic su **[!UICONTROL View]** per elencare i profili disponibili.

   ![](../../assets/offers_simulation-add-profile.png)

1. Aggiungi altri profili per testare dati di profilo diversi e salvare la selezione.

   ![](../../assets/offers_simulation-save-profiles.png)

1. Una volta aggiunto, tutti i profili sono elencati nell’elenco a discesa in **[!UICONTROL Test profile]**. Puoi passare da un profilo di test salvato all’altro per visualizzare i risultati per ciascun profilo selezionato.

   ![](../../assets/offers_simulation-saved-profiles.png)

1. Puoi fare clic su **[!UICONTROL Profile details]** per visualizzare i dati di profilo selezionati.

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## Aggiungi ambiti decisionali

Ora seleziona le decisioni di offerta da simulare sui profili di test.

1. Seleziona **[!UICONTROL Add decision scope]**.

   ![](../../assets/offers_simulation-add-decision.png)

1. Seleziona un posizionamento dall’elenco.

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. Vengono visualizzate le decisioni disponibili.

   * Puoi utilizzare il campo di ricerca per perfezionare la selezione.
   * Puoi fare clic su **[!UICONTROL Open offer decisions]** per aprire l&#39;elenco di tutte le decisioni create. Ulteriori informazioni su [decisioni](create-offer-activities.md).

   Seleziona la scelta e fai clic su **[!UICONTROL Add]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. L&#39;ambito decisionale appena definito viene visualizzato nell&#39;area di lavoro principale.

   Puoi regolare il numero di offerte che desideri richiedere. Ad esempio, se selezioni 2, verranno visualizzate le migliori 2 offerte per questo ambito decisionale.

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Puoi richiedere fino a 30 offerte.

1. Ripeti i passaggi precedenti per aggiungere tutte le decisioni necessarie.

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Anche se definisci diversi ambiti decisionali, viene simulata una sola richiesta API.
   >
   >Tutti i flag di deduplicazione sono abilitati per impostazione predefinita per la simulazione, il che significa che il motore decisionale consente i duplicati e può quindi fare la stessa proposta in più decisioni. Per saperne di più sul [!DNL Decisions] Proprietà di richiesta API in [questa sezione](../api-reference/decisions-api/deliver-offers.md).

## Visualizza risultati di simulazione

Dopo aver aggiunto un ambito decisionale e selezionato un profilo di test, puoi visualizzare i risultati.

1. Fai clic su **[!UICONTROL View results]**.

   ![](../../assets/offers_simulation-view-results.png)

1. Le migliori offerte disponibili vengono visualizzate in base al profilo selezionato per ogni decisione.

   Seleziona un’offerta per visualizzarne i dettagli.

   ![](../../assets/offers_simulation-offer-details.png)

1. Seleziona un altro profilo dall’elenco per visualizzare i risultati delle decisioni relative all’offerta per un diverso profilo di test.

1. È possibile aggiungere, rimuovere o aggiornare gli ambiti decisionali il numero di volte necessario.

>[!NOTE]
>
>Ogni volta che modifichi un profilo o aggiorni un ambito decisionale, devi aggiornare i risultati utilizzando **[!UICONTROL View results]** pulsante .

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->