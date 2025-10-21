---
title: Aggiornare una raccolta di elementi
description: Le raccolte sono sottoinsiemi di offerte basate su condizioni predefinite definite da un addetto marketing, ad esempio la categoria dell’offerta.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: a2b7779d-8c2e-4ff9-8cc3-90846f100c98
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '132'
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
