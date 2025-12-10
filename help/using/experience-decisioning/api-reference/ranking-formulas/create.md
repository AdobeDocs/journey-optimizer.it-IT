---
title: Creare una formula di classificazione
description: Le formule di classificazione consentono di definire le funzioni per il punteggio, utilizzate per classificare gli elementi.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 2eb3ca65-f9f2-4483-ac6a-7bd896b0e516
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 16%

---

# Creare una formula di classificazione {#create-ranking-formula}

Per creare una formula di classificazione, effettua una richiesta POST all’API Libreria di offerte.

**Intestazioni Accept e Content-Type**

La tabella seguente mostra i valori validi che comprendono i campi Content-Type nell’intestazione della richiesta:

| Nome intestazione | Valore |
| --------- | ----------- | 
| Content-Type | application/json |

**Formato API**

```http
POST /{ENDPOINT_PATH}/ranking-formulas 
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |

**Richiesta**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/ranking-formulas' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Test Ranking Function DPS",
    "description": "Ranking  function description",
    "exdFunction": true,
    "returnType": {
        "type": "integer"
    },
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "if(offer.rank.priority.isNotNull(), offer.rank.priority, 0) * if(offer.tags.intersects(boosted.tags), 2, 1)"
    },
    "definedOn": {
        "offer": {
            "schema": {
                "altId": "_experience.offer-management.personalized-offer",
                "version": "0"
            }
        },
        "boosted": {
            "schema": {
                "altId": "_xdm.context.foo",
                "version": "0"
            }
        }
    }
}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli della formula di classificazione appena creata, incluso `id`. È possibile utilizzare `id` nei passaggi successivi per aggiornare o eliminare la formula di classificazione.

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
