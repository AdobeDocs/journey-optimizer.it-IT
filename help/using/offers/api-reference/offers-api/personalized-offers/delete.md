---
title: Eliminare le offerte personalizzate
description: Un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 9%

---

# Eliminare un’offerta personalizzata {#delete-personalized-offer}

A volte può essere necessario rimuovere (DELETE) un’offerta personalizzata. A tale scopo, è necessario eseguire una richiesta DELETE all&#39;API [!DNL Offer Library] utilizzando l&#39;ID dell&#39;offerta personalizzata che si desidera eliminare.

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

Puoi confermare l’eliminazione tentando di inviare una richiesta di ricerca (GET) a personalized-offer. Dovresti ricevere lo stato HTTP 404 (Non trovato) perché l’offerta personalizzata è stata rimossa.
