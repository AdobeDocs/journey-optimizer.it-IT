---
title: Creare un qualificatore di raccolta
description: I qualificatori di raccolta consentono di organizzare e ordinare meglio le offerte.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: f3f7cccb-0173-409e-8b76-8b6e136a22ac
source-git-commit: 835e4bf227ce330b1426a9a4331fdf533fc757e3
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 12%

---

# Creare un qualificatore di raccolta {#create-tag}

È possibile creare un qualificatore di raccolta (noto in precedenza come &quot;tag&quot;) effettuando una richiesta di POST al [!DNL Offer Library] , fornendo al tempo stesso l&#39;ID del contenitore.

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

Nella tabella seguente sono riportati i valori validi che comprendono *Content-Type* e *Accetta* campi nell’intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano i qualificatori della raccolta. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Richiesta**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1; schema="https://ns.adobe.com/experience/offer-management/tag;version=0.1"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Holiday sales and promotions"
    }'
```

**Risposta**

Una risposta corretta restituisce informazioni sul qualificatore di raccolta appena creato, compreso l’ID di istanza univoco e il posizionamento `@id`. Puoi utilizzare l’ID istanza in passaggi successivi per aggiornare o eliminare il qualificatore della raccolta. Puoi utilizzare il tuo qualificatore di raccolta univoco `@id` in esercitazioni successive per creare raccolte e offerte personalizzate.

```json
{
    "instanceId": "d48fd160-13dc-11eb-bc55-c11be7252432",
    "@id": "xcore:tag:124e147572cd7866",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:34:34.486296Z",
    "repo:lastModifiedDate": "2020-10-21T20:34:34.486296Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```
