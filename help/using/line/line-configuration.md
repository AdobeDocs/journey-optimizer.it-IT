---
solution: Journey Optimizer
product: journey optimizer
title: Configurare il canale LINE
description: Scopri come configurare il tuo ambiente per inviare messaggi LINE con Journey Optimizer
feature: Line, Channel Configuration
role: Admin
level: Intermediate
exl-id: 8ad0e57b-6bdc-43b0-9511-31e2ac1be1f9
TQID: https://experienceleague.adobe.com/yDRCVzfdPGXisgxJ59UT8HYsdXI82H07Ol--YP7wmE0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 365
ht-degree: 8%

---

# Configurare il canale LINE in Journey Optimizer {#line-configuration}

1. Accedi al menu **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni generali]** > **[!UICONTROL Configurazioni canale]**, quindi fai clic su **[!UICONTROL Crea configurazione canale]**.

   ![](assets/line-config-1.png)

1. Immetti un nome e una descrizione (facoltativa) per la configurazione, quindi seleziona il canale da configurare.

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri trattino basso `_`, punto `.` e trattino `-`.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base alla configurazione, è possibile selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

1. Seleziona il canale **LINE**.

   ![](assets/line-config-2.png)

1. Seleziona **[!UICONTROL Azione di marketing]** per associare i criteri di consenso ai messaggi utilizzando questa configurazione. Tutti i criteri di consenso associati all’azione di marketing vengono utilizzati per rispettare le preferenze dei clienti. [Ulteriori informazioni](../action/consent.md#surface-marketing-actions)

1. Seleziona il tipo di messaggio per la configurazione:

   * **Marketing**: per messaggi promozionali, ad esempio promozioni settimanali per un negozio al dettaglio. Questi messaggi richiedono il consenso dell’utente e devono essere conformi alla politica di LINE relativa alle opzioni di consenso dell’utente.
   * **Transazionale**: per messaggi non commerciali, ad esempio conferme di ordini, notifiche di reimpostazione della password o aggiornamenti di consegna. Questi messaggi possono essere inviati anche agli utenti che hanno annullato l’abbonamento alle comunicazioni di marketing, ma sono strettamente limitati a contesti transazionali specifici.

1. Seleziona le **[!UICONTROL impostazioni canale]**.

   Rivolgiti al tuo rappresentante Adobe per configurare le **[!UICONTROL impostazioni del canale]**.

   ![](assets/line-config-2.png)

1. Seleziona il tuo **[!UICONTROL ID utente LINE]** da mappare. Questo è l’identificatore utilizzato per collegare i messaggi a singoli utenti all’interno del tuo canale LINE.

1. Digita il **[!UICONTROL Nome mittente]**, ad esempio il nome del tuo marchio.

1. Invia le modifiche.

Ora puoi selezionare la configurazione durante la creazione del messaggio LINE.

## Configurare l’API delle impostazioni del canale LINE {#line-api}

Questa API configura le impostazioni del canale che memorizzano i dettagli di autorizzazione e configurazione necessari per la connessione all’API di messaggistica LINE. Queste impostazioni consentono a Adobe Journey Optimizer di autenticare e inviare messaggi tramite LINE utilizzando le credenziali fornite.

**Endpoint**

```
POST https://platform.adobe.io/journey/imp/config/channel-settings
```

| Nome intestazione | Descrizione |
|-|-|
| Authorization | Token utente dal tuo account tecnico |
| x-api-key | ID client da Adobe Developer Console |
| x-gw-ims-org-id | ID organizzazione IMS |
| x-sandbox-name | Nome della sandbox, ad esempio prod |
| Content-Type | Deve essere application/json |


**Corpo richiesta**

```json
{
    "name": "your_defined_name",
    "channelRegistryId": "line",
    "channel": "line",
    "channelSettings": {
        "channelId": "your_line_channel_id",
        "channelSecret": "your_line_channel_secret"
    }
}
```

**Risposta impostazioni canale**

```json
{
"id": "3603ed66-ae86-42b8-8a90-d4b4e54e7c3b",
"name": "your_defined_name",
"channelRegistryId": "line",
"channel": "line",
"channelSettings": {
    "channelId": "your_line_channel_id",
    "channelSecret": "your_line_channel_secret"
    },
    "channelPublicationId": "v1_line",
    "createdAt": "2025-07-30T12:00:00.000Z",
    "modifiedAt": "2025-07-30T12:00:00.000Z",
    "isFromLatestVersion": true,
    "_etag": "\"eab98d24-18af-48ae-90f9-e59d4f8cfb2b\""
}
```
