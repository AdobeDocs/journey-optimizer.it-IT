---
title: Aggiornare formule di classificazione
description: Le formule di classificazione consentono di definire le funzioni per il punteggio, utilizzate per classificare gli elementi.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
exl-id: 4ef1bfc2-e74f-4b44-b3b5-8a4f2fbd6438
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 9%

---

# Aggiornare una formula di classificazione {#update-ranking-formula}

Puoi modificare o aggiornare una formula di classificazione effettuando una richiesta PUT all’API Libreria di offerte.

Per ulteriori informazioni sul PUT JSON, incluse le operazioni disponibili, consulta la [documentazione ufficiale sul PUT JSON](http://jsonpatch.com/).

**Intestazioni Accept e Content-Type**

La tabella seguente mostra i valori validi che comprendono i campi Content-Type nell’intestazione della richiesta:

| Nome intestazione | Valore |
| --------- | ----------- |
| Content-Type | `application/json` |

**Formato API**

```http
PUT /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da aggiornare. | `rankingFormula1234` |

**Richiesta**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "[UPDATED] Test Ranking Function DPS",
    "description": "Ranking  function description",
    "isPure": true,
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

| Parametro | Descrizione |
| --------- | ----------- |
| `value` | Il nuovo valore con cui desideri aggiornare il parametro. |
| `path` | Percorso del parametro da aggiornare. |
| `op` | Chiamata di operazione utilizzata per definire l&#39;azione necessaria per aggiornare la connessione. Le operazioni includono: `add`, `replace`, `remove`, `copy` e `test`. |

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli aggiornati della formula di classificazione, incluso l’ID.

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
