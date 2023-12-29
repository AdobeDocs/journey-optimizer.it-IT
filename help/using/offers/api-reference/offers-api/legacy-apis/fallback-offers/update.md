---
title: Aggiornare un’offerta di fallback
description: Un’offerta di fallback viene inviata ai clienti se non sono idonei per altre offerte
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f153c2ee-e789-4d8e-a03b-e914690ff354
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 11%

---

# Aggiornare un’offerta di fallback {#update-fallback-offer}

Puoi modificare o aggiornare un’offerta di fallback nel contenitore effettuando una richiesta PATCH al [!DNL Offer Library] API.

Per ulteriori informazioni sulla patch JSON, comprese le operazioni disponibili, consulta la sezione [Documentazione delle patch JSON](https://jsonpatch.com/).

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che compongono *Content-Type* e *Accetta* campi nell’intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato API**

```http
PATCH /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le offerte di fallback. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID istanza dell’offerta di fallback. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Richiesta**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated fallback offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated fallback offer description"
    }
]'
```

| Parametro | Descrizione |
| --------- | ----------- |
| `op` | Chiamata di operazione utilizzata per definire l&#39;azione necessaria per aggiornare la connessione. Le operazioni includono: `add`, `replace`, e `remove`. |
| `path` | Percorso del parametro da aggiornare. |
| `value` | Il nuovo valore con cui desideri aggiornare il parametro. |

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli aggiornati dell’offerta di fallback, inclusa la sua istanza univoca `id`.

```json
{
    "id": "{ID}",
    "datasetId": "{DATASET_ID}",
    "sandboxId": "{SANDBOX_ID}",
    "etag": 2,
    "createdDate": "2023-09-07T12:47:43.012Z",
    "lastModifiedDate": "2023-09-07T12:47:43.012Z",
    "createdBy": "{CREATED_BY}",
    "lastModifiedBy": "{MODIFIED_BY}",
    "createdByClientId": "{CREATED_CLIENT_ID}",
    "lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
