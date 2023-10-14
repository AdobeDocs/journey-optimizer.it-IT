---
title: Eliminare una raccolta
description: Le raccolte sono sottoinsiemi di offerte basate su condizioni predefinite definite da un addetto marketing, ad esempio la categoria dell’offerta.
feature: Offers, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 11%

---

# Eliminare una raccolta {#delete-collection}

Talvolta può essere necessario rimuovere (DELETE) una raccolta. Questa operazione viene eseguita eseguendo una richiesta DELETE al [!DNL Offer Library] API tramite `id` della raccolta che desideri eliminare.

**Formato API**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da eliminare. | `offerCollection1234` |

**Richiesta**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce lo stato HTTP 200 e un corpo vuoto.

Puoi confermare l’eliminazione tentando di inviare una richiesta di ricerca (GET) alla raccolta. Dovresti ricevere lo stato HTTP 404 (Non trovato) perché la raccolta è stata rimossa.
