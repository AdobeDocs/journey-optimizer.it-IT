---
title: Aggiorna posizionamento exd
description: Il posizionamento Exd consiste in raccolte associate a vincoli e metodi di classificazione per determinare le offerte.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
version: Journey Orchestration
exl-id: 74e090e1-4dbe-484b-a482-ef43e082e7b1
TQID: https://experienceleague.adobe.com/6RpNeMQUn2qEfAzQ-Q7f7PgBRJCLqp7WnsoKx0xr12s
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 7%

---

# Aggiornare un posizionamento exd {#update-exd-placement}

Per modificare o aggiornare un posizionamento, effettua una richiesta PUT all’API Libreria di offerte.

Per ulteriori informazioni sul PUT JSON, comprese le operazioni disponibili, consulta la documentazione ufficiale sul PUT JSON.

**Intestazioni Accept e Content-Type**

La tabella seguente mostra i valori validi che comprendono i campi Content-Type nell’intestazione della richiesta:

| Parametro | Descrizione |
| --------- | ----------- |
| Content-Type | `application/json` |

**Formato API**

```http
PUT /{ENDPOINT_PATH}/exd-placements/{ID}
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID dell’entità da aggiornare. | `placement1234` |

**Richiesta**

```shell
curl --location --request PUT 'https://platform-stage.adobe.io/data/core/dps/exd-placements/dps:exd-placement:19aca09b0a456e57' \
--H 'Content-Type: application/json' \
--H 'x-gw-ims-org-id: {IMS_ORG}' \
--H 'x-sandbox-name: {SANDBOX_NAME}' \
--H 'x-api-key: {API_KEY}' \
--H 'Authorization: Bearer {ACCESS_TOKEN}' \
--X '{
  "id":"dps:exd-placement:19aca09b0a456e57",
  "description": "Keyboard application",
  "status":"archived"
}'
```

| Parametro | Descrizione |
| --------- | ----------- |
| `value` | Il nuovo valore con cui desideri aggiornare il parametro. |
| `path` | Percorso del parametro da aggiornare. |
| `op` | Chiamata di operazione utilizzata per definire l&#39;azione necessaria per aggiornare la connessione. Le operazioni includono: `add`, `replace`, `remove`, `copy` e `test`. |

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli aggiornati del posizionamento exd, incluso l’ID.

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
