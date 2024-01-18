---
title: Aggiorna qualificatori raccolta
description: I qualificatori di raccolta ti consentono di organizzare e ordinare meglio le offerte.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 918927e1-ad7a-4937-b652-2a0932e9efa1
source-git-commit: ba7d065523116c12e22eec300df13c29d92a54fb
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 10%

---


# Aggiornare un qualificatore di raccolta {#update-collection-qualifier}

Puoi modificare o aggiornare un qualificatore di raccolta (precedentemente noto come &quot;tag&quot;) effettuando una richiesta PATCH all’API Libreria di offerte.

Per ulteriori informazioni sulla patch JSON, comprese le operazioni disponibili, consulta la sezione [Documentazione delle patch JSON](https://jsonpatch.com/).

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che compongono *Content-Type* nell’intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato API**

```http
PATCH /{ENDPOINT_PATH}/tags/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID dell’entità da aggiornare. | `tag1234` |

**Richiesta**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated tag"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated tag description"
    }
]'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli aggiornati del qualificatore di raccolta, incluso il relativo univoco `id`.

```json
{
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 2,
    "createdDate": "2023-09-07T12:36:26.602Z",
    "lastModifiedDate": "2023-09-07T12:36:26.602Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
