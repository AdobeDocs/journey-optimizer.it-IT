---
solution: Journey Optimizer
product: journey optimizer
title: Creare un messaggio di attività live
description: Scopri come creare un’attività Live in Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: 9864a136-e129-4279-bb09-081b72f584df
TQID: https://experienceleague.adobe.com/orXAhry8onHXUejP5pzOyHdKbAcD8fiDmvRk-s74xLo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
  - id: ed2fba79-65cb-4680-96d2-2ad5d851714d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: e4d9ae1971d435c221107bede26abe3f74983a6f
workflow-type: tm+mt
source-wordcount: 726
ht-degree: 6%

---

# Creare un’attività live {#create-mobile-live}

>[!BEGINSHADEBOX]

**In questa pagina:** crea una campagna attivata da API in Journey Optimizer in modo da poter avviare, aggiornare e terminare in remoto le attività Live per singoli utenti o tipi di pubblico.

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

   >[!NOTE]
   >
   >Per le campagne **Marketing attivato da API**, puoi selezionare un pubblico esistente che funga da prima segmentazione prima di controllare la sottoscrizione al channelID APN dal payload API.

1. Le campagne sono progettate per essere eseguite in una data specifica o con una frequenza ricorrente. Scopri come configurare la **[!UICONTROL pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

1. Una volta configurata, fai clic su **[!UICONTROL Verifica per attivare]**, quindi fai clic su **[!UICONTROL Attiva]**.

1. Dopo l&#39;attivazione della campagna, utilizza la **richiesta cURL** fornita come modello per attivare gli eventi di inizio, aggiornamento o fine dell&#39;attività Live. Aggiorna il payload di esempio con i dati specifici prima dell’esecuzione.

   Assicurati anche di copiare gli identificatori **[!UICONTROL ID campagna]** da includere nel payload.

   ➡️ Per informazioni sui requisiti di autenticazione, inclusi token OAuth e chiavi API, consulta la [documentazione di campagne attivate da API](https://developer.adobe.com/journey-optimizer-apis/references/messaging).

   ![](assets/create-live-3.png)

   +++ Esempio di un payload per casi d’uso unitari (campagna transazionale attivata da API)

   Questo esempio di payload è destinato a singole campagne che utilizzano il tipo di campagna **Transazionale** attivato da API. La maggior parte dei campi del seguente esempio di payload sono obbligatori, solo `requestId`, `dismissal-date` e `alert` sono facoltativi.

   ```json
   {
       "requestId": "your-request-id",
       "campaignId": "your-campaign-id",
       "recipients": [
   {
       "type": "aep",
       "userId": "testemail@gmail.com",
       "namespace": "email",
       "context": {
        "requestPayload": {
       "aps": {
       "content-available": 1,
       "timestamp": 1756984054,              // current epoch time
       "dismissal-date": 1756984084,         // optional – auto remove when event="end"
       "event": "update",                    // start | update | end
   
       // Fields from FoodDeliveryLiveActivityAttributes
       "content-state": {
         "orderStatus": "Delivered"
       },
   
       "attributes-type": "FoodDeliveryLiveActivityAttributes",
       "attributes": {
         "restaurantName": "Pizza",
         "liveActivityData": {
           "liveActivityID": "orderId1"       // customer reference ID
         }
       },
   
       "alert": {
         "title": "Order Delivered!",
         "body": "Your pizza has arrived."
       }
     }
   }
   }
   }
   ]
   }
   ```

   +++

   +++ Esempio di payload per casi d’uso di broadcast (campagna di marketing attivata da API)

   Questo esempio di payload è per le campagne basate su pubblico che utilizzano il tipo di campagna Marketing **attivato da API**.

   ```json
   {
       "requestId": "123400000",
       "campaignId": "d32e6f6c-56df-4a98-a2c0-6db6008f8f32",
       "audience": {
           "id": "508f9416-52d0-4898-ba47-08baaa22e9c7"
       },
       "context": {
           "requestPayload": {
               "aps": {
                   "input-push-channel": "V+8UslywEfAAAOq9SbTrLg==",  //apns-channel-id
                   "content-available": 1,
                   "timestamp": 1770808339,
                   "event": "update",   // start | update | end
   
                   // Fields from GameScoreLiveActivityAttributes
                   "content-state": {
                       "homeTeamScore": 33,
                       "awayTeamScore": 49,
                       "statusText": "Wingdom keeps scoring!"
                   },
                   "attributes-type": "GameScoreLiveActivityAttributes",
                   "attributes": {
                       "liveActivityData": {
                           "channelID": "V+8UslywEfAAAOq9SbTrLg=="   //apns-channel-id, must match the "input-push-channel" value
                       }
                   },
                   "alert": {
                       "title": "This is the title for game",
                       "body": "This is the body for body"
                   }
               }
           }
       }
   }
   ```

   +++

Dopo aver progettato la tua attività Live, puoi monitorare la misurazione dell&#39;impatto della tua attività Live con [rapporti incorporati](../reports/campaign-global-report-cja-activity.md).

>[!TIP]
>
>Se la tua attività Live non viene visualizzata o aggiornata come previsto, consulta [Risoluzione dei problemi relativi alle attività Live](troubleshoot-mobile-live.md) per istruzioni dettagliate sul debug.

## Aggiungere dati personalizzati con i metadati di esecuzione {#metadata}

>[!AVAILABILITY]
>
> `executionMetadata` è disponibile per entrambe le campagne **Transazionale attivato da API** e **Marketing attivato da API**.

Allega i tuoi **dati personalizzati** a un profilo, ad esempio un ID ordine, un livello fedeltà o un codice di regione, utilizzando il campo facoltativo `executionMetadata`. Journey Optimizer archivia questi dati insieme all&#39;esecuzione in modo da poterli recuperare in seguito dal set di dati **Feedback attività live** e far corrispondere i risultati della consegna ai tuoi record aziendali.

Per inviare questi dati tramite API, vedere il riferimento all&#39;API di messaggistica [per il campo `executionMetadata`](https://developer.adobe.com/journey-optimizer-apis/references/messaging#operation/postIMUnitaryMessageExecution!path=recipients/0/executionMetadata&t=request). Per leggere nuovamente i valori sul dispositivo, consulta la [guida di Mobile SDK sulla ricezione dei metadati di esecuzione dal trigger API](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/live-activities/tutorial#receiving-execution-metadata-from-the-api-trigger).

Per aggiungere dati personalizzati con i metadati di esecuzione:

* Aggiungi `executionMetadata` a un profilo, accanto a `userId` e `namespace`. Sono accettate solo le chiavi e i valori stringa. Converti qualsiasi valore non stringa in una stringa prima di inviarla.

* I valori vengono registrati esattamente come inviati. `executionMetadata` non supporta espressioni di personalizzazione, pertanto qualsiasi espressione `{{...}}` viene trattata come testo letterale anziché risolta. Dovresti sempre inviare valori letterali finali.

* Ogni profilo può contenere fino a **50 coppie chiave/valore**, con un limite di dimensioni combinate di **2 KB** per tutte le chiavi e i valori. I metadati che superano questo limite vengono scartati, ma l’attività Live viene comunque consegnata. Limita il payload alle informazioni richieste a scopo di reporting.

+++ Esempio JSON

In questo esempio, `orderId`, `tier`, `restaurant` e `region` sono valori personalizzati. Una volta attivata l’attività Live, puoi leggerla nuovamente dal set di dati di feedback per collegare la consegna al record dell’ordine.

```json
{
    "requestId": "your-request-id",
    "campaignId": "your-campaign-id",
    "recipients": [
        {
            "type": "aep",
            "userId": "testemail@gmail.com",
            "namespace": "email",
            "executionMetadata": {
                "orderId": "A-123",
                "tier": "gold",
                "restaurant": "PizzaPlace",
                "region": "EU"
            },
            "context": {
                "requestPayload": {
                    "aps": {
                        "content-available": 1,
                        "timestamp": 1756984054,
                        "dismissal-date": 1756984084,
                        "event": "update",
                        "content-state": {
                            "orderStatus": "Delivered"
                        },
                        "attributes-type": "FoodDeliveryLiveActivityAttributes",
                        "attributes": {
                            "restaurantName": "PizzaPlace",
                            "liveActivityData": {
                                "liveActivityID": "orderId1"
                            }
                        },
                        "alert": {
                            "title": "Order Delivered!",
                            "body": "Your pizza has arrived."
                        }
                    }
                }
            }
        }
    ]
}
```

+++

## Video dimostrativo

Scopri come configurare iOS Live Activities con Adobe Journey Optimizer per offrire aggiornamenti avanzati e in tempo reale nella schermata di blocco di iPhone e su Dynamic Island.

>[!VIDEO](https://video.tv.adobe.com/v/3479864)
