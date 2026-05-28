---
title: Ricercare un elemento di decisione
description: Gli elementi decisionali sono offerte di marketing che puoi creare e organizzare in raccolte e cataloghi.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 8a4e09ec-57bc-48ad-b626-6a15ba987791
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/xJsgp0F-4jph6z67eXTMlwFFU02BE8dJzGg8KbJ5IBY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 8%

---

# Ricercare un elemento di decisione {#lookup-decision-items}

Per cercare elementi decisionali specifici effettuando una richiesta GET all’API della Libreria di offerte che include l’ID nel percorso della richiesta.

**Formato API**

```http
GET /{ENDPOINT_PATH}/offer-items/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da cercare. | `offerItem1234` |

**Richiesta**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli dell’elemento decisione.

```json
{
    "created": "2024-06-10T16:00:34.014Z",
    "modified": "2024-07-09T22:59:21.507Z",
    "etag": 1,
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "offerItem5678",
    "_experience": {
        "decisioning": {
            "offeritem": {
                "fCapConstraintsLastIndex": 0,
                "lifecycleStatus": "approved"
            },
            "decisionitem": {
                "itemCalendarConstraints": {
                    "endDate": "2030-12-31T08:00:00.000Z",
                    "startDate": "2024-06-10T04:00:00.000Z"
                },
                "itemCatalogID": "itemCatalong1234",
                "itemConstraints": {
                    "eligibilityRule": "rule1234",
                    "profileConstraintType": "eligibilityRule"
                },
                "itemDescription": "Offer item description",
                "itemID": "offerItem5678",
                "itemLabels": [],
                "itemName": "Offer Item One",
                "itemPriority": 1,
                "itemTags": []
            }
        }
    },
    "_<imsOrg>": {
        "some_field": "some value"
    }
}
```
