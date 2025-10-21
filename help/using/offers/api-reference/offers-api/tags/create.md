---
title: Creare un qualificatore di raccolta
description: I qualificatori di raccolta ti consentono di organizzare e ordinare meglio le offerte.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 14%

---


# Creare un qualificatore di raccolta {#create-tag}

Per creare un qualificatore di raccolta (precedentemente noto come &quot;tag&quot;), devi effettuare una richiesta POST all’API della Libreria di offerte.

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che comprendono i campi *Content-Type* nell&#39;intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/tags
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |

**Richiesta**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/tags' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{        
    "name": "Black Friday",
    "description": "Tag for black friday"
}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce informazioni sul nuovo qualificatore di raccolta creato, incluso il relativo `id` univoco. È possibile utilizzare `id` nei passaggi successivi per aggiornare o eliminare il qualificatore della raccolta. È possibile utilizzare il qualificatore di raccolta univoco `id` nelle esercitazioni successive per creare raccolte e offerte personalizzate.

```json
{
    "id": "{ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 1,
    "createdDate": "2023-09-07T12:36:26.602Z",
    "lastModifiedDate": "2023-09-07T12:36:26.602Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
