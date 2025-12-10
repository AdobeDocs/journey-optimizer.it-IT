---
title: Ricercare una formula di classificazione
description: Le formule di classificazione consentono di definire le funzioni per il punteggio, utilizzate per classificare gli elementi.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: f048b2d1-d26b-4987-8acb-3558df506ec2
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 8%

---

# Ricercare un  {#list-ranking-formula}

Per cercare una formula di classificazione specifica, effettua una richiesta GET all’API Libreria di offerte che include l’ID nel percorso della richiesta.

**Formato API**

```http
GET /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da cercare. | `rankingFormula1234` |

**Richiesta**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli della formula di classificazione.

```json
{
    "created": "2024-08-08T23:45:15.380Z",
    "modified": "2024-10-22T18:15:05.909Z",
    "etag": 36,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/ranking-function"
    ],
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "id": "dps:ranking-function:1947f5372cc4ed74",
    "name": "[Do not delete] - Cypress e2e - edit",
    "description": "some description",
    "returnType": {
        "type": "INTEGER"
    },
    "exdFunction": true,
    "expression": {
        "type": "PQL",
        "format": "pql/text",
        "value": "42 = 11"
    }
}
```
