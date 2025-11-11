---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Cercare un qualificatore di raccolta
description: I qualificatori di raccolta ti consentono di organizzare e ordinare meglio le offerte.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: e2d1f093-c1b8-4c4c-a20f-4bd7c2ea5269
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# Cercare un qualificatore di raccolta {#look-up-tag}

Per cercare qualificatori di raccolta specifici (noti in precedenza come &quot;tag&quot;), devi effettuare una richiesta GET all’API della Libreria di offerte che includa l’ID qualificatore della raccolta nel percorso della richiesta.

**Formato API**

```http
GET /{ENDPOINT_PATH}/tags/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID dell’entità da cercare. | `tag1234` |

**Richiesta**

```shell
curl -X GET 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Accept: *,application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli del qualificatore di raccolta, incluse le informazioni sull&#39;ID contenitore, l&#39;ID istanza e il qualificatore di raccolta univoco `@id`.

```json
{
    "created": "2022-09-16T19:00:02.070+00:00",
    "modified": "2022-09-16T19:00:02.070+00:00",
    "etag": 1,
    "schemas": [
        "https://ns.adobe.com/experience/offer-management/tag;version=0.1"
    ],
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "id": "tag1234",
    "name": "Sneakers"
}
```
