---
title: Eliminare un’offerta di fallback
description: Un’offerta di fallback viene inviata ai clienti se non sono idonei per altre offerte
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 12%

---


# Eliminare un’offerta di fallback {#delete-fallback-offer}

A volte può essere necessario rimuovere (DELETE) un’offerta di fallback. Questa operazione viene eseguita eseguendo una richiesta DELETE all&#39;API [!DNL Offer Library] utilizzando l&#39;ID dell&#39;offerta di fallback che si desidera eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID dell’entità da eliminare. | `fallbackOffer1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando di inviare una richiesta di ricerca (GET) all’offerta; in caso contrario, riceverai lo stato HTTP 404 (Non trovato) perché l’offerta di fallback è stata rimossa.
