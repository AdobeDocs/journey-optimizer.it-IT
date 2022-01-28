---
title: Creare simulazioni
description: Scopri come creare simulazioni
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 39b52f39ec19c185d2cd95634a60e37f62a66f83
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 1%

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
   >Per impostazione predefinita, tutti i flag Deduplication sono abilitati per la simulazione, il che significa che il motore decisionale consente i duplicati e può quindi fare la stessa proposta in più decisioni/posizionamenti. Per saperne di più sul [!DNL Decisions] Proprietà di richiesta API in [questa sezione](../api-reference/decisions-api/deliver-offers.md).<!--Deduplication note TO REMOVE WHEN SIMULATIONS V2 is on PROD-->

<!--SIMULATIONS V2

## Define simulation settings {#define-simulation-settings}

To edit the default settings for your simulations, follow the steps below.

1. Click **[!UICONTROL Settings]**.

    ![](../../assets/offers_simulation-settings.png)

1. In the **[!UICONTROL Deduplication]** section, you can choose to allow duplicate offers accross decisions and/or placements. It means that multiple decisions/placements may get assigned the same offer.

    ![](../../assets/offers_simulation-settings-deduplication.png)

    >[!NOTE]
    >
    >By default, all Deduplication flags are enabled for simulation, which means that the decision engine allows duplicates and thus can make the same proposition accross multiple decisions/placements. Learn more on the [!DNL Decisions] API request properties in [this section](../api-reference/decisions-api/deliver-offers.md).

1. In the **[!UICONTROL Response format]** section, you can choose to include metadata in the code view. Check the corresponding option, and select the metadata of your choice. They will be displayed in the request and response payloads when selecting **[!UICONTROL View code]**. Learn more in the [View simulation results](#simulation-results) section.

    ![](../../assets/offers_simulation-settings-response-format.png)

    >[!NOTE]
    >
    >When turning on the option, all items are selected by default.

1. Click **[!UICONTROL Save]**.-->

<!--NOT FOR SIMULATIONS V2

In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context Data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## Visualizza risultati di simulazione {#simulation-results}

Dopo aver aggiunto un ambito decisionale e selezionato un profilo di test, puoi visualizzare i risultati.

1. Fai clic su **[!UICONTROL View results]**.

   ![](../../assets/offers_simulation-view-results.png)

1. Le migliori offerte disponibili vengono visualizzate in base al profilo selezionato per ogni decisione.

   Seleziona un’offerta per visualizzarne i dettagli.

   ![](../../assets/offers_simulation-offer-details.png)

   <!--
    SIMULATIONS V2
    1. Click **[!UICONTROL View code]** to display the request and response payloads. [Learn more](#view-code)-->

1. Seleziona un altro profilo dall’elenco per visualizzare i risultati delle decisioni relative all’offerta per un diverso profilo di test.

1. È possibile aggiungere, rimuovere o aggiornare gli ambiti decisionali il numero di volte necessario.

>[!NOTE]
>
>Ogni volta che modifichi un profilo o aggiorni un ambito decisionale, devi aggiornare i risultati utilizzando **[!UICONTROL View results]** pulsante .

<!--
SIMULATIONS V2

## View code {#view-code}

To use the request payload outside of [!DNL Journey Optimizer] - for troubleshooting purpose for example, you can copy it by clicking the corresponding button on top of the code view.
    
>[!NOTE]
>
>You cannot copy the response payload.

Below is an example of code view:

    ```
    curl -X POST \
    'https://platform.adobe.io/data/core/ode/{CONTAINER_ID}/decisions' \
    -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
    -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
    -H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsIng1dSI6Imltc19uYTEtc3RnMS1rZXktMS5jZXIifQ.eyJpZCI6IjE2NDMxMzg3NDMxODlfOTIzY2ZjZjgtOWVkYy00MjE1LWJjODgtYmEyYTY2ZGIyYmMyX3VlMSIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJjbGllbnRfaWQiOiJhY3BfdWlfcGxhdGZvcm0iLCJ1c2VyX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJzdGF0ZSI6IntcInNlc3Npb25cIjpcImh0dHBzOi8vaW1zLW5hMS1zdGcxLmFkb2JlbG9naW4uY29tL2ltcy9zZXNzaW9uL3YxL1l6azNNakE0TXpNdFpXVTVaUzAwTVdOaExUZ3pNamd0TmpFM1pqZ3lOak5qTmpSakxTMDBPRVExTnpRM1FUWXdOemMyUkVSRk1FRTBPVFF3TVVSQVFXUnZZbVZKUkFcIn0iLCJhcyI6Imltcy1uYTEtc3RnMSIsImFhX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJjdHAiOjAsImZnIjoiV0VQQTNUSUY0UjRaQTZEWlBDUk1BMklBQ1U9PT09PT0iLCJzaWQiOiIxNjQzMDYwMDg0NzI2XzYzNGJkNDEzLWMwYTktNDA0NS1iNTM3LWRmMzgzYzU5ZGIxY191ZTEiLCJydGlkIjoiMTY0MzEzODc0MzE4OV9lYWMxOWY5Yi00ZjhhLTQ1NWMtOWVmMi1mNjYwNmQ0ODY4N2ZfdWUxIiwibW9pIjoiYmVjOTQzYzIiLCJwYmEiOiIiLCJvYyI6InJlbmdhKm5hMXItc3RnMSoxN2U5MmIzNzYzNCo2MEJEVjBGUlhOMFlRMkdHSkRON0E5Tk1HOCIsInJ0ZWEiOiIxNjQ0MzQ4MzQzMTg5IiwiZXhwaXJlc19pbiI6Ijg2NDAwMDAwIiwic2NvcGUiOiJvcGVuaWQsc2Vzc2lvbixyZWFkX29yZ2FuaXphdGlvbnMsYWRkaXRpb25hbF9pbmZvLnByb2plY3RlZFByb2R1Y3RDb250ZXh0LGFkZGl0aW9uYWxfaW5mby5yb2xlcyxhdWRpZW5jZW1hbmFnZXJfYXBpLEFkb2JlSUQiLCJjcmVhdGVkX2F0IjoiMTY0MzEzODc0MzE4OSJ9.TgZ998KHA4Zeoyq7b_NbPv8aPHb2cs9GgP3uJKrTbzosylKKRYqLpj_8HkloI-bFVQFCBCOWbCwtJtkcRIvFlQFruTr5bpMatPV8izEUVutO6smkYBFoGFYyEGuN5Xe97uOJZEHzFSWguGZtgttSrNhXr-j0hFloofjXDJXPB_911dzXALp5s15sd3HLH9XWTwwlqF_a5SMNDXaSj1800RxsB9bJ8_YL0x4pqQwjYJxRGMhiy7Y9IOpwogSBEiqCQitlKYgaO7yaJzFwhfyisnqM7_MWX2ETn-kGFEOoBHxXDTx9P2OPojzb8ChWQgmGf7Expyvtc1ke3nJkppzrxg' \
    -H 'x-api-key: {API_KEY}' \
    -H 'x-gw-ims-org-id: 5D1328435BF324E90A49402A@AdobeOrg' \
    -H 'x-sandbox-name: prod' \
    -D '{
      "xdm:propositionRequests": [
            {
                  "xdm:placementId": "xcore:offer-placement:1416f4109d9d292c",
                  "xdm:activityId": "xcore:offer-activity:1416f4aad9fd99d7",
                  "xdm:itemCount": 2
            }
      ],
      "xdm:profiles": [
            {
                  "xdm:identityMap": {
                        "email": [
                              {
                                    "xdm:id": "poyfair@adobe.com"
                              }
                        ]
                  }
            }
      ],
      "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
      },
      "xdm:responseFormat": {
            "xdm:includeMetadata": {
                  "xdm:activity": [],
                  "xdm:option": [],
                  "xdm:placement": []
            }
      }
    }'
    ```

>[!NOTE]
>
>When copying the request payload into your own code, make sure you replace CONTAINER_ID and API_KEY with your own values.-->

