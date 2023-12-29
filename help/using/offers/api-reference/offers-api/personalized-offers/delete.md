---
title: Eliminare le offerte personalizzate
description: Un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 9%

---

# Eliminare un’offerta personalizzata {#delete-personalized-offer}

Occasionalmente può essere necessario rimuovere (DELETE) un’offerta personalizzata. Questa operazione viene eseguita eseguendo una richiesta DELETE al [!DNL Offer Library] API che utilizza l’ID dell’offerta personalizzata che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID dell’entità da eliminare. | `personalizedOffer1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando una richiesta di ricerca (GET) a personalized-offer e riceverai uno stato HTTP 404 (Non trovato) perché l’offerta personalizzata è stata rimossa.
