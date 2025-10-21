---
title: Creare un posizionamento exd
description: Le strategie Exd sono costituite da raccolte associate a vincoli e metodi di classificazione per determinare le offerte.
feature: Decision Management, API, Collections
topic: Integrations
role: Developer
level: Experienced
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 8%

---

# Creare un posizionamento exd {#create-exd-placement}

Per creare un posizionamento exd, devi eseguire una richiesta POST all’API Libreria di offerte.

**Intestazioni Accept e Content-Type**

La tabella seguente mostra i valori validi che comprendono i campi Content-Type nell’intestazione della richiesta:

| Parametro | Descrizione |
| --------- | ----------- |
| Content-Type | `application/json` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/exd-placements
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps` |

**Richiesta**

```shell
curl --location 'https://platform-stage.adobe.io/data/core/dps/exd-placements' \
--header 'Content-Type: application/json' \
--header 'x-gw-ims-org-id: {IMS_ORG}' \
--header 'x-sandbox-name: {SANDBOX_NAME}' \
--header 'x-api-key: {API_KEY}' \
--header 'Authorization: Bearer {ACCESS_TOKEN}' \
--data '{
  "name": "Test Exd Placement1 Pants",
  "channel": "https://ns.adobe.com/xdm/channel-types/email",
  "tags":["3d75b849-b344-402b-9d9e-5d750bd46884"],
  "channelConfiguration":"530b76f9-dcd6-4fd5-8c52-38e29b04a60a",
  "description": "compressing alarm",
  "status":"active"
}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli del posizionamento exd appena creato, incluso l’ID. Puoi utilizzare l’ID nei passaggi successivi per aggiornare o eliminare il posizionamento exd.

```json
{
    "id": "dps:exd-placement:19cb038eca47bead",
    "sandboxId": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "etag": 2,
    "createdDate": "2024-11-18T18:48:56.298Z",
    "lastModifiedDate": "2024-11-18T18:57:27.457Z",
    "createdBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedBy": "71486D7B5F4011980A494030@AdobeID",
    "lastModifiedByClientId": "CJMTestClientACP"
}
```
