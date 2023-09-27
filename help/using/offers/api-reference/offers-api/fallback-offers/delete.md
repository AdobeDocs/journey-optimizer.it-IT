---
title: Eliminare un’offerta di fallback
description: Un’offerta di fallback viene inviata ai clienti se non sono idonei per altre offerte
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 12%

---


# Eliminare un’offerta di fallback {#delete-fallback-offer}

A volte può essere necessario rimuovere (DELETE) un’offerta di fallback. Questa operazione viene eseguita eseguendo una richiesta DELETE al [!DNL Offer Library] API che utilizza l’ID dell’offerta di fallback che desideri eliminare.

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
