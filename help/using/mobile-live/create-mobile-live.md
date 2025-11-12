---
solution: Journey Optimizer
product: journey optimizer
title: Creare un messaggio di attività live
description: Scopri come creare un’attività Live in Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: ce6bfca78d097588b5958c10c721b29b7013b3e2
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 1%

---

# Creare un’attività Live {#create-mobile-live}

>[!BEGINSHADEBOX]

* [Introduzione all’attività live](get-started-mobile-live.md)
* [Configurazione attività live](mobile-live-configuration.md)
* [Integrazione di Live Activity con Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* **[Crea un&#39;attività live](create-mobile-live.md)**
* [Domande frequenti](mobile-live-faq.md)
* [Rapporto campagna attività live](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

Dopo aver configurato la configurazione mobile e aver implementato il SDK mobile di Adobe Experience Platform, puoi iniziare a creare la tua attività Live in Journey Optimizer:

1. Accedi al menu **[!UICONTROL Campagne]**, quindi fai clic su **[!UICONTROL Crea campagna]**.

1. Seleziona il tipo di campagna **API attivata**.

   * Seleziona **Marketing attivato da API** per campagne basate su pubblico

   * Seleziona **Transazionale attivato da API** per le singole campagne.

   >[!IMPORTANT]
   >
   > Tieni presente che per **Transazionale attivato da API**, l&#39;opzione **[!UICONTROL Alta velocità effettiva]** non deve essere abilitata.


   ![](assets/create-live-1.png)

1. Dalla sezione **[!UICONTROL Proprietà]**, modifica il **[!UICONTROL Titolo]** e la **[!UICONTROL Descrizione]** della tua campagna.

1. Nella sezione **[!UICONTROL Azioni]**, scegli **[!UICONTROL Attività live]** e seleziona o crea una nuova configurazione.

   Ulteriori informazioni sulla configurazione delle attività live in [questa pagina](mobile-live-configuration.md).

   ![](assets/create-live-2.png)

1. Fai clic su **[!UICONTROL Crea esperimento]** per iniziare a configurare l&#39;esperimento sui contenuti e creare trattamenti per misurarne le prestazioni e identificare l&#39;opzione migliore per il pubblico di destinazione. [Ulteriori informazioni](../content-management/content-experiment.md)

1. Dalla scheda **[!UICONTROL Pubblico]**, scegli il tuo **[!UICONTROL Tipo di identità]** [Ulteriori informazioni](../audience/about-audiences.md).

1. Le campagne sono progettate per essere eseguite in una data specifica o con una frequenza ricorrente. Scopri come configurare la **[!UICONTROL pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

1. Una volta configurata, fai clic su **[!UICONTROL Verifica per attivare]**, quindi fai clic su **[!UICONTROL Attiva]**.

1. Dopo l&#39;attivazione della campagna, utilizza la **richiesta cURL** fornita come modello per attivare gli eventi di inizio, aggiornamento o fine dell&#39;attività Live. Aggiorna il payload di esempio con i dati specifici prima dell’esecuzione.

   Assicurati anche di copiare gli identificatori **[!UICONTROL ID campagna]** da includere nel payload.

   ➡️ Per informazioni sui requisiti di autenticazione, inclusi token OAuth e chiavi API, consulta la [documentazione di campagne attivate da API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/).

   ![](assets/create-live-3.png)

   +++ Esempio di un singolo payload

   La maggior parte dei campi del seguente esempio di payload sono obbligatori, solo `requestId`, `dismissal-date` e `alert` sono facoltativi.

       &quot;json
       {
       &quot;requestId&quot;: &quot;your-request-id&quot;,
       &quot;campaignId&quot;: &quot;your-campaign-id&quot;,
       &quot;destinatari&quot;: [
       {
       &quot;type&quot;: &quot;aep&quot;,
       &quot;userId&quot;: &quot;testemail@gmail.com&quot;,
       &quot;namespace&quot;: &quot;email&quot;,
       &quot;contesto&quot;: {
       &quot;requestPayload&quot;: {
       &quot;aps&quot;: {
       &quot;contenuto disponibile&quot;: 1,
       &quot;timestamp&quot;: 1756984054,              // ora attuale
       &quot;dismissal-date&quot;: 1756984084,         // facoltativo - rimozione automatica quando event=&quot;end&quot;
       &quot;event&quot;: &quot;update&quot;,                    // inizio | aggiorna | fine
       
       // Campi da FoodDeliveryLiveActivityAttributes
       &quot;content-state&quot;: {
       &quot;orderStatus&quot;: &quot;Consegnato&quot;
       },
       
       &quot;attributes-type&quot;: &quot;FoodDeliveryLiveActivityAttributes&quot;,
       &quot;attributi&quot;: {
       &quot;RestaurantName&quot;: &quot;Pizza&quot;,
       &quot;liveActivityData&quot;: {
       &quot;liveActivityID&quot;: &quot;orderId1&quot;       // ID riferimento cliente
       }
       },
       
       &quot;avviso&quot;: {
       &quot;title&quot;: &quot;Ordine consegnato!&quot;,
       &quot;body&quot;: &quot;La tua pizza è arrivata.&quot;
       }
       }
       }
       }
       }
       ]
       }
       &quot;
   +++

Dopo aver progettato la tua attività Live, puoi monitorare la misurazione dell&#39;impatto della tua attività Live con [rapporti incorporati](../reports/campaign-global-report-cja-activity.md).
