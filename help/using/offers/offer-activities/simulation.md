---
title: Creare simulazioni
description: Scopri come simulare quali offerte verranno consegnate per un determinato posizionamento al fine di convalidare la logica decisionale
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: f50617dc5ea07d01d1f7ec1ab3f9790557dcd957
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 1%

---

# Creare simulazioni {#create-simulations}

## Informazioni sulla simulazione {#about-simulation}

Per convalidare la logica decisionale, puoi simulare quali offerte verranno consegnate a un profilo di test per un determinato posizionamento.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Questo ti consente di testare e perfezionare diverse versioni delle offerte senza alcun impatto sui destinatari interessati.

>[!NOTE]
>
>Questa funzionalità simula una singola richiesta al [!DNL Decisioning] API. Ulteriori informazioni su [Consegnare offerte tramite l’API Decisioning](../api-reference/offer-delivery-api/decisioning-api.md).

Per accedere a questa funzione, seleziona la **[!UICONTROL Simulation]** dalla scheda **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** menu.

![](../assets/offers_simulation-tab.png)

>[!NOTE]
>
>Poiché la simulazione non genera alcun evento decisionale, il [tappatura](../offer-library/creating-personalized-offers.md#capping) il conteggio non è interessato.

<!--
➡️ [Discover this feature in video](#video)
-->

## Selezionare i profili di test {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation_test_profile"
>title="Aggiungere profili di test"
>abstract="Puoi aggiungere un profilo di test selezionando uno spazio dei nomi di identità e un valore di identità corrispondente. È necessario che i profili di test siano già disponibili per poterli utilizzare per la simulazione."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/segment/profiles/creating-test-profiles.html" text="Crea profili di test"

Innanzitutto devi selezionare i profili di test che utilizzerai per la simulazione.

>[!CAUTION]
>
>Devi disporre di profili di test per simulare quali offerte verranno consegnate loro. Scopri come [creare profili di test](../../segment/creating-test-profiles.md).

1. Fai clic su **[!UICONTROL Manage profile]**.

   ![](../assets/offers_simulation-manage-profile.png)

1. Seleziona lo spazio dei nomi di identità da utilizzare per identificare i profili di test. In questo esempio, utilizzeremo il **E-mail** spazio dei nomi.

   >[!NOTE]
   >
   >Uno spazio dei nomi di identità definisce il contesto di un identificatore, ad esempio un indirizzo e-mail o un ID CRM. Ulteriori informazioni sui namespace delle identità Adobe Experience Platform [in questa sezione](../../segment/get-started-identity.md){target=&quot;_blank&quot;}.

1. Immetti il valore dell&#39;identità e fai clic su **[!UICONTROL View]** per elencare i profili disponibili.

   ![](../assets/offers_simulation-add-profile.png)

1. Aggiungi altri profili per testare dati di profilo diversi e salvare la selezione.

   ![](../assets/offers_simulation-save-profiles.png)

1. Una volta aggiunto, tutti i profili sono elencati nell’elenco a discesa in **[!UICONTROL Test profile]**. Puoi passare da un profilo di test salvato all’altro per visualizzare i risultati per ciascun profilo selezionato.

   ![](../assets/offers_simulation-saved-profiles.png)

   >[!NOTE]
   >
   >I profili selezionati rimarranno elencati come profili di test nel **[!UICONTROL Simulation]** scheda da sessione a sessione fino a quando non vengono rimosse utilizzando **[!UICONTROL Manage profile]**.

1. Puoi fare clic su **[!UICONTROL Profile details]** per visualizzare i dati di profilo selezionati.

<!--Learn more on [selecting test profiles](messages/preview.md#select-test-profiles)-->

## Aggiungi ambiti decisionali {#add-decision-scopes}

Ora seleziona le decisioni di offerta da simulare sui profili di test.

1. Seleziona **[!UICONTROL Add decision scope]**.

   ![](../assets/offers_simulation-add-decision.png)

1. Seleziona un posizionamento dall’elenco.

   ![](../assets/offers_simulation-add-decision-scope.png)

1. Vengono visualizzate le decisioni disponibili.

   * Puoi utilizzare il campo di ricerca per perfezionare la selezione.
   * Puoi fare clic su **[!UICONTROL Open offer decisions]** per aprire l&#39;elenco di tutte le decisioni create. Ulteriori informazioni su [decisioni](create-offer-activities.md).

   Seleziona la scelta e fai clic su **[!UICONTROL Add]**.

   ![](../assets/offers_simulation-add-decision-scope-add.png)

1. L&#39;ambito decisionale appena definito viene visualizzato nell&#39;area di lavoro principale.

   Puoi regolare il numero di offerte che desideri richiedere. Ad esempio, se selezioni 2, verranno visualizzate le migliori 2 offerte per questo ambito decisionale.

   ![](../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Puoi richiedere fino a 30 offerte.

1. Ripeti i passaggi precedenti per aggiungere tutte le decisioni necessarie.

   ![](../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Anche se definisci diversi ambiti decisionali, viene simulata una sola richiesta API.

## Definire le impostazioni di simulazione {#define-simulation-settings}

Per modificare le impostazioni predefinite per le simulazioni, segui i passaggi riportati di seguito.

1. Fai clic su **[!UICONTROL Settings]**.

   ![](../assets/offers_simulation-settings.png)

1. In **[!UICONTROL Deduplication]** puoi scegliere di consentire offerte duplicate per decisioni e/o posizionamenti. Ciò significa che a più decisioni/posizionamenti può essere assegnata la stessa offerta.

   ![](../assets/offers_simulation-settings-deduplication.png)

   >[!NOTE]
   >
   >Per impostazione predefinita, tutti i flag Deduplication sono abilitati per la simulazione, il che significa che il motore decisionale consente i duplicati e può quindi fare la stessa proposta in più decisioni/posizionamenti. Per saperne di più sul [!DNL Decisioning] Proprietà di richiesta API in [questa sezione](../api-reference/offer-delivery-api/decisioning-api.md).

1. In **[!UICONTROL Response format]** è possibile scegliere di includere i metadati nella vista Codice. Seleziona l’opzione corrispondente e seleziona i metadati desiderati. Verranno visualizzati nei payload di richiesta e risposta al momento della selezione **[!UICONTROL View code]**. Ulteriori informazioni nel [Visualizza risultati di simulazione](#simulation-results) sezione .

   ![](../assets/offers_simulation-settings-response-format.png)

   >[!NOTE]
   >
   >Quando l’opzione è attivata, per impostazione predefinita vengono selezionati tutti gli elementi.

1. Fai clic su **[!UICONTROL Save]**.

>[!NOTE]
>
>Attualmente per i dati di simulazione puoi utilizzare solo il **[!UICONTROL Hub]** API.

<!--
In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## Visualizza risultati di simulazione {#simulation-results}

Dopo aver aggiunto un ambito decisionale e selezionato un profilo di test, puoi visualizzare i risultati.

1. Fai clic su **[!UICONTROL View results]**.

   ![](../assets/offers_simulation-view-results.png)

1. Le migliori offerte disponibili vengono visualizzate in base al profilo selezionato per ogni decisione.

   Seleziona un’offerta per visualizzarne i dettagli.

   ![](../assets/offers_simulation-offer-details.png)

1. Fai clic su **[!UICONTROL View code]** per visualizzare i payload di richiesta e risposta. [Ulteriori informazioni](#view-code)

1. Seleziona un altro profilo dall’elenco per visualizzare i risultati delle decisioni relative all’offerta per un diverso profilo di test.

1. È possibile aggiungere, rimuovere o aggiornare gli ambiti decisionali il numero di volte necessario.

>[!NOTE]
>
>Ogni volta che modifichi un profilo o aggiorni un ambito decisionale, devi aggiornare i risultati utilizzando **[!UICONTROL View results]** pulsante .

## Visualizza codice {#view-code}

1. Utilizza la **[!UICONTROL View code]** per visualizzare i payload di richiesta e risposta.

   ![](../assets/offers_simulation-view-code.png)

   La vista Codice mostra le informazioni per gli sviluppatori relative all&#39;utente corrente. Per impostazione predefinita, la **[!UICONTROL Response payload]** viene visualizzato.

   ![](../assets/offers_simulation-request-payload.png)

1. Fai clic su **[!UICONTROL Response payload]** o **[!UICONTROL Request payload]** per spostarsi tra le due schede.

   ![](../assets/offers_simulation-response-payload.png)

1. Per utilizzare il payload della richiesta al di fuori di [!DNL Journey Optimizer] - per la risoluzione dei problemi, ad esempio, copialo utilizzando **[!UICONTROL Copy to clipboard]** nella parte superiore della vista codice.

   ![](../assets/offers_simulation-copy-payload.png)

   <!--You cannot copy the response payload. ACTUALLY YES YOU CAN > to confirm with PM/dev? -->

   >[!NOTE]
   >
   >Quando copi i payload di richiesta o risposta nel tuo codice, assicurati di sostituire {USER_TOKEN} e {API_KEY} con valori validi. Scopri come recuperare questi valori nel [API di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html)Documentazione di {target=&quot;_blank&quot;}.

