---
solution: Journey Optimizer
product: journey optimizer
title: Creare webhook di feedback per campagne attivate da API in Journey Optimizer
description: Scopri come creare webhook di feedback per campagne attivate da API in Journey Optimizer.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
source-git-commit: be07b0dfec31d23f741bfc2a9f89fe1a7891ef0b
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---


# Creare webhook di feedback per campagne attivate da API {#webhooks}

I webhook di feedback consentono di ricevere aggiornamenti di stato in tempo reale per i messaggi inviati tramite campagne attivate dall’API transazionale. Configurando un webhook, puoi ricevere automaticamente i risultati di consegna direttamente ai sistemi, abilitando il monitoraggio, la registrazione e l’elaborazione automatizzata.

Puoi gestire le configurazioni del webhook dal menu **[!UICONTROL Impostazioni del webhook di amministrazione]** / **[!UICONTROL Canali]** / **[!UICONTROL Feedback]**.

![](assets/webhook-list.png)

>[!NOTE]
>È consentita una sola configurazione webhook per combinazione di **organizzazione + sandbox**.

## Creare un webhook di feedback

Per creare un webhook, effettua le seguenti operazioni:

1. Passa a **[!UICONTROL Amministrazione]** / **[!UICONTROL Canali]** / **[!UICONTROL Impostazioni webhook feedback]**.

1. Fai clic su **Crea webhook feedback**.

1. Nella sezione **[!UICONTROL Configurazione di base]**, fornisci i seguenti dettagli:

   ![](assets/webhook-config.png)

   * **Nome webhook** - Immettere un nome descrittivo per identificare il webhook.
   * **Canali** - Seleziona i canali per i quali questo webhook deve ricevere feedback (e-mail e/o SMS).
   * **URL webhook** - Fornisci l&#39;endpoint HTTPS in cui devono essere consegnati gli eventi di feedback.

1. Nella sezione **[!UICONTROL Autenticazione]** selezionare il metodo di autenticazione:

   ![](assets/webhook-authentication.png)

   * **Nessuna autenticazione** - Nessuna intestazione di autenticazione aggiunta.
   * **Autenticazione JWT** - Fornisci i dettagli richiesti se l&#39;endpoint richiede l&#39;autenticazione JWT.

1. Nella sezione **[!UICONTROL Parametri intestazione]**, configura intestazioni personalizzate aggiuntive da inviare con ogni richiesta webhook.

   ![](assets/webhook-header.png)

1. Fai clic su **[!UICONTROL Invia]** per salvare la configurazione.

>[!NOTE]
>
>È possibile modificare un webhook in qualsiasi momento. Per farlo, aprirlo dall&#39;inventario e fare clic sul pulsante **[!UICONTROL Modifica]**.

## Struttura del payload del webhook

Dopo l&#39;esecuzione di un messaggio, **[!DNL Journey Optimizer]** invia il payload seguente all&#39;endpoint configurato.

```
{
  "requestId": "8NoByJneShCdCGRnrGS1t1m3CdA73dhR",
  "imsOrg": "myImsOrg",
  "sandbox": {
    "id": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "name": "prod"
  },
  "channel": "email",
  "eventType": "message.feedback",
  "messageExecution": {
    "messageExecutionID": "HUMA-26362805",
    "messageType": "transactional",
    "campaignID": "16f24a15-7e21-477c-848a-d5695ca7f137",
    "campaignVersionID": "2ca10c10-56dd-4505-87cd-fa5da84e7a5d"
  },
  "messageDeliveryFeedback": {
    "feedbackStatus": {
      "value": "bounce"
    },
    "offers": null,
    "messageExclusion": null,
    "messageFailure": {
      "category": "sync",
      "type": "Ignored",
      "code": "25",
      "reason": "Admin Failure"
    },
    "retryCount": 0
  },
  "identityMap": {
    "email": [
      {
        "id": "john.doe@luma.com",
        "primary": true
      }
    ]
  }
}
```

Il webhook può acquisire i seguenti eventi:

* Inviate
* Consegnate
* Mancato recapito (vedi l’esempio precedente)
* Errori

Ogni richiesta in ingresso include anche un requestId univoco che viene rimandato al webhook.

## Passaggi successivi {#next}

Una volta creato un webhook di feedback, puoi abilitarlo durante la configurazione di un pubblico di **campagna attivata da API transazionali**. Per ulteriori informazioni, consulta questa sezione: [Abilita webhook](../campaigns/api-triggered-campaign-audience.md#webhook)
