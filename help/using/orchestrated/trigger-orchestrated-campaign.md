---
solution: Journey Optimizer
product: journey optimizer
title: Attivare una campagna orchestrata utilizzando un segnale
description: Scopri come attivare una campagna orchestrata utilizzando un segnale in [!DNL Adobe Journey Optimizer].
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
source-git-commit: c9a5c29c685cf21fda2b5df1a3838713e054f696
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 0%

---


# Attivare campagne orchestrate utilizzando un segnale {#trigger-signal}

Puoi attivare una campagna orchestrata inviandole un segnale invece di eseguirla secondo una pianificazione. Il segnale viene inviato tramite una chiamata API da un sistema o un’applicazione esterna. Quando utilizzi un segnale, puoi trasmettere parametri. Vengono quindi rese disponibili nella campagna orchestrata come variabili evento nel contesto di esecuzione, per l’utilizzo in targeting, condizioni o espressioni.

Processo end-to-end per attivare una campagna orchestrata utilizzando un segnale:

1. [Pianificare l’attivazione della campagna da parte di un segnale](#set-an-orchestrated-campaign-to-wait-for-a-signal-configure-signal)
1. [Aggiungi parametri per il payload del segnale](#add-parameters-for-the-signal-payload-optional-parameters) (facoltativo)
1. [Creare e testare la campagna](#build-and-test-the-campaign-build-and-test)
1. [Pubblicare e attivare la campagna](#publish-and-trigger-the-campaign-publish)

## Pianificare l’attivazione della campagna da parte di un segnale {#configure-signal}

Per impostare una campagna orchestrata in modo che inizi su un segnale invece che su una pianificazione, effettua le seguenti operazioni:

1. Apri la campagna orchestrata che desideri attivare utilizzando un segnale.

1. Apri la configurazione della pianificazione. [Scopri come pianificare una campagna orchestrata](create-orchestrated-campaign.md#schedule).

1. Seleziona **[!UICONTROL Attivato da un segnale]** in modo che la campagna attenda un segnale invece di essere eseguita secondo una pianificazione.

   ![Menu Pianifica con attivazione da un&#39;opzione di segnale selezionata](assets/triggered-oc-scheduler.png){zoomable="yes"}

## Aggiungere parametri per il payload del segnale (facoltativo) {#parameters}

Puoi trasmettere parametri nel segnale di attivazione e utilizzarli nella campagna nel contesto di esecuzione, ad esempio nel targeting, nelle condizioni o nelle espressioni. Definisci prima ciascun parametro nelle impostazioni di pianificazione, quindi trasmettine il relativo valore quando chiami l&#39;API dell&#39;attivatore.

1. Apri il modulo di pianificazione campagne e seleziona **[!UICONTROL Aggiungi parametro]**.

1. Definisci il nome e il tipo di dati di ciascun parametro da inviare nel payload del segnale. Puoi anche fornire **valori di test** che verranno utilizzati quando attivi la campagna in modalità di test. [Scopri come verificare una campagna attivata](#build-and-test).

   ![Aggiungi il parametro per definire i parametri di payload per il segnale](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>Se nella chiamata API trasmetti un parametro che non è stato definito nella pianificazione, la chiamata API ha comunque esito positivo e il parametro viene propagato, quindi puoi utilizzarlo nelle espressioni. Tuttavia, l’interfaccia orchestrata della campagna non ti aiuterà a utilizzarla, ad esempio, l’attività Test non elencherà o mostrerà parametri non definiti nell’utilità di pianificazione.

## Creare e testare la campagna {#build-and-test}

Crea la campagna sull’area di lavoro, quindi, facoltativamente, testala in bozza attivando il segnale tramite l’API prima della pubblicazione.

1. Aggiungi e connetti attività (pubblico, targeting, consegne) sull’area di lavoro. [Scopri come orchestrare le attività della campagna](orchestrate-activities.md)

1. Se hai definito i parametri nel segnale, puoi collegarli alla logica dell’area di lavoro (ad esempio, in condizioni o nel targeting). In questo esempio, il parametro &quot;channel&quot; viene utilizzato come condizione in un&#39;attività **[!UICONTROL Test]**.

   ![Parametro canale utilizzato come condizione nell&#39;attività di test](assets/triggered-oc-use-parameters.png)

   Per utilizzare un parametro di segnale nell&#39;editor espressioni (ad esempio, per generare una query in un&#39;attività **[!UICONTROL Genera pubblico]**), digitare `$(vars/@<parameterName>)` nel campo espressione. Sostituire `<parameterName>` con il nome del parametro definito nella pianificazione, ad esempio `$(vars/@channel)`. [Scopri come utilizzare l&#39;editor espressioni](edit-expressions.md).

1. Apri l&#39;utilità di pianificazione della campagna, seleziona **[!UICONTROL Copia richiesta API]** e scegli il formato (cURL o richiesta HTTP).

   Le informazioni copiate includono l’ID della campagna orchestrata, il nome della sandbox, l’ID organizzazione e i valori di test per i parametri, se ne hai aggiunti alcuni.

   ![Opzione Copia richiesta API nella configurazione di pianificazione](assets/triggered-oc-copy.png)

   +++Richiesta cURL di esempio con un parametro e un valore di test

   ```bash
   POST https://platform.adobe.io/ajo/campaign-orchestration/orchestratedCampaigns/1c7529c7-7a8c-491a-a2c6-3d8131d2e17d/trigger
   
   Headers:
   Authorization: Bearer ## Access token ##
   Content-Type: application/json
   x-api-key: ## Provide API Key here ##
   x-api-version: 1
   x-gw-ims-org-id: 123456ABCDEFG@LumaOrg
   x-sandbox-name: prod
   
   Body:
   {
   "variables": {
      "channel": "sms"
   }
   }
   ```

   +++

1. Fai clic su **[!UICONTROL Inizio]** per avviare la campagna.

1. Invia la chiamata API del trigger utilizzando la richiesta di esempio copiata dal modulo di pianificazione. <!--For the complete API reference, refer to the [Journey Optimizer API documentation](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}.-->

Quando si è soddisfatti dei risultati del test, [pubblicare la campagna](#publish).

## Pubblicare e attivare la campagna {#publish}

Dopo aver generato e testato [la campagna](#build-and-test), pubblicala in modo che possa essere attivata dall&#39;applicazione.

1. Fai clic su **[!UICONTROL Pubblica]** nell&#39;area di lavoro della campagna. La campagna deve essere pubblicata prima di poter essere attivata da un sistema esterno. [Ulteriori informazioni sull&#39;avvio e il monitoraggio della campagna](start-monitor-campaigns.md#publish).

1. Apri l&#39;utilità di pianificazione della campagna, seleziona **[!UICONTROL Copia richiesta API]** e scegli il formato (cURL o richiesta HTTP).

   Le informazioni copiate includono l’ID della campagna orchestrata, il nome della sandbox, l’ID dell’organizzazione e i parametri, se ne hai aggiunti alcuni.

   ![Copia richiesta API nella configurazione di pianificazione](assets/triggered-oc-copy.png)

1. Chiama l&#39;API del trigger dal sistema.

   >[!IMPORTANT]
   >
   >Per una campagna orchestrata in tempo reale, un guardrail della velocità impone un **intervallo minimo di un&#39;ora** tra due esecuzioni del trigger API. Se si chiama di nuovo l&#39;API prima che l&#39;intervallo sia trascorso, l&#39;API restituisce l&#39;errore **HTTP 429** (troppe richieste). Questo guardrail non viene applicato quando si attiva una versione bozza per testarla.

   Se hai aggiunto parametri al payload del segnale, i valori trasmessi nella chiamata API vengono esposti come variabili evento della campagna durante l’esecuzione della campagna. Per esaminarli, apri i registri della campagna dalla barra degli strumenti dell’area di lavoro della campagna. Nella scheda **[!UICONTROL Attività]**, identifica l&#39;attività corrispondente al segnale e fai clic sull&#39;icona a forma di matita per accedere alle variabili di evento correlate. [Scopri come accedere a registri e attività](start-monitor-campaigns.md#logs-tasks).

   ![Schermata Registri e attività in cui sono disponibili le variabili evento della campagna](assets/trigger-events-variables.png){zoomable="yes"}
