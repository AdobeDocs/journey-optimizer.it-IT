---
title: Aggiornare una raccolta di elementi
description: Le raccolte sono sottoinsiemi di offerte basate su condizioni predefinite definite da un addetto marketing, ad esempio la categoria dell’offerta.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: a2b7779d-8c2e-4ff9-8cc3-90846f100c98
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qYudO0NFgw9zjq843wK8zVMwr-nk29HPdXAHLBUc7qg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 6%

---

# Aggiornare una raccolta di elementi {#update-item-collection}

Per modificare o aggiornare una raccolta di elementi, devi eseguire una richiesta PATCH all’API Libreria di offerte.

Per ulteriori informazioni sulla patch JSON, incluse le operazioni disponibili, consulta la [documentazione ufficiale sulla patch JSON](https://jsonpatch.com/).

**Formato API**

```http
PATCH /{ENDPOINT_PATH}/item-collections/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da aggiornare. | `itemCollections1234` |

**Richiesta**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated item collection"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated item collection description"
    }
]'
```

| Parametro | Descrizione |
| --------- | ----------- |
| `value` | Il nuovo valore con cui desideri aggiornare il parametro. |
| `path` | Percorso del parametro da aggiornare. |
| `op` | Chiamata di operazione utilizzata per definire l&#39;azione necessaria per aggiornare la connessione. Le operazioni includono: `add`, `replace`, `remove`, `copy` e `test`. |

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli aggiornati della raccolta di elementi, incluso `id`.

```json
{
    "etag": 2,
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
