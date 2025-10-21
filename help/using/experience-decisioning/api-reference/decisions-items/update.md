---
title: Aggiornare un elemento di decisione
description: Gli elementi decisionali sono offerte di marketing che puoi creare e organizzare in raccolte e cataloghi.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: b924b7d0-bbed-409e-8173-0685fc41d7de
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 6%

---

# Aggiornare un elemento di decisione {#update-decision-items}

Per modificare o aggiornare un elemento decisionale, effettua una richiesta PATCH all’API Libreria di offerte.

Per ulteriori informazioni sulla patch JSON, incluse le operazioni disponibili, consulta la [documentazione ufficiale sulla patch JSON](https://jsonpatch.com/).

**Formato API**

```http
PATCH /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da aggiornare. | `offerItem1234` |

**Richiesta**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}' \
-d '[
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemName",
        "value": "Updated offer item"
    },
    {
        "op": "replace",
        "path": "/_experience/decisioning/decisionitem/itemDescription",
        "value": "Updated offer item description"
    }
]'
```

| Parametro | Descrizione |
| --------- | ----------- |
| `value` | Il nuovo valore con cui desideri aggiornare il parametro. |
| `path` | Percorso del parametro da aggiornare. |
| `op` | Tipo di operazione da eseguire. Le operazioni includono: `add`, `replace`, `remove`, `copy` e `test`. |

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli dell’elemento aggiornato, incluso l’ID. Puoi utilizzare l’ID nei passaggi successivi per aggiornare o eliminare l’elemento decisionale.

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
