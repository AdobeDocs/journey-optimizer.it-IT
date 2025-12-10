---
title: Creare una raccolta di elementi
description: Le raccolte ti consentono di categorizzare e raggruppare gli elementi decisionali in base alle tue preferenze.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: e4f2ab34-2af2-49b5-9164-b129e922fe59
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 8%

---

# Creare una raccolta di elementi {#create-decision-items}

Per creare una raccolta di elementi, devi eseguire una richiesta POST all’API Libreria di offerte.

**Formato API**

```http
POST /{ENDPOINT_PATH}/item-collections
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |

**Richiesta**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/item-collections' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{     
    "name": "Item collection One",
    "description": "Item collection",
    "constraints": [
        {
            "itemCatalogId": "itemCatalog1234",
            "uiModel": "{\"operator\":\"equals\",\"value\":{\"left\":\"_experience.decisioning.decisionitem.itemName\",\"right\":\"Some offer item\"}}"
        }
    ]
}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli del nuovo elemento di decisione creato, incluso l’ID. Puoi utilizzare l’ID nei passaggi successivi per aggiornare o eliminare l’elemento decisionale.

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
