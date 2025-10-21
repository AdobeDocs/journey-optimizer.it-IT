---
title: Creare una raccolta
description: Le raccolte sono sottoinsiemi di offerte basate su condizioni predefinite definite da un addetto marketing, ad esempio la categoria dell’offerta.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 683f8b86-8545-46d0-a4a8-25c5b3c7b9c3
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 12%

---

# Creare una raccolta {#create-collection}

Le raccolte sono sottoinsiemi di offerte basate su condizioni predefinite definite da un addetto marketing, ad esempio la categoria dell’offerta.

È possibile creare una raccolta effettuando una richiesta POST all&#39;API [!DNL Offer Library].

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che costituiscono il campo *Content-Type* nell&#39;intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/offer-collections
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |

**Richiesta**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-collections' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Collection with tags",
    "filterType": "any-tags",
    "ids": [
        "tag1234"
    ],
    "labels": [
        "core/C5",
        "custom/myLabel"
    ]
}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce informazioni sulla raccolta appena creata, incluso `id`. È possibile utilizzare `id` nei passaggi successivi per aggiornare o eliminare la raccolta o in un&#39;esercitazione successiva per creare una decisione.

```json
{
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "createdDate": "2023-05-31T15:09:11.771Z",
    "lastModifiedDate": "2023-05-31T15:09:11.771Z",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
