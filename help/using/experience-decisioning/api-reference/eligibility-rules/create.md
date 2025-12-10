---
title: Creare una regola di idoneità
description: Le regole di idoneità consentono di definire i candidati idonei in base a ciò di cui desideri eseguire il targeting, ad esempio gli attributi di profilo e i tipi di pubblico.
feature: API, Collections, Decisioning
role: Developer
level: Experienced
exl-id: 39c6e82e-c1b1-4dda-a941-3db6324cef37
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 7%

---

# Creare una regola di idoneità {#create-eligibility-rule}

Per creare una regola di idoneità, devi effettuare una richiesta POST all’API della Libreria di offerte.

**Formato API**

```http
POST /{ENDPOINT_PATH}/eligibility-rules 
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |

**Richiesta**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '
{
    "name": "test dule",
    "description": "xxxxxx",
    "exdRule": true,
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "inSegment(\"849807b6-0a76-4895-96d9-89996477f23b\") and billingAddress.city.equals(\"san jose\", false)"
    }
}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli della regola di idoneità appena creata, incluso l’ID. Puoi utilizzare l’ID nei passaggi successivi per aggiornare o eliminare la regola di idoneità.

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
