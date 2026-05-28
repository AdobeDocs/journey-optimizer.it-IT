---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Aggiornare un’offerta di fallback
description: Un’offerta di fallback viene inviata ai clienti se non sono idonei per altre offerte
feature: Decision Management, API
badge: label="Legacy" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: f153c2ee-e789-4d8e-a03b-e914690ff354
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/LS2tnWXKdj2cFf-VFEJd-tygvnE48dyi2JAKSejsxZ8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 186
ht-degree: 20%

---

# Aggiornare un’offerta di fallback {#update-fallback-offer}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../../../../experience-decisioning/gs-experience-decisioning.md)


È possibile modificare o aggiornare un&#39;offerta di fallback nel contenitore effettuando una richiesta PATCH all&#39;API [!DNL Offer Library].

Per ulteriori informazioni sulla patch JSON, incluse le operazioni disponibili, consulta la [documentazione ufficiale sulla patch JSON](https://jsonpatch.com/).

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che comprendono i campi *Content-Type* e *Accept* nell&#39;intestazione della richiesta:

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
| `op` | Chiamata di operazione utilizzata per definire l&#39;azione necessaria per aggiornare la connessione. Le operazioni includono: `add`, `replace` e `remove`. |
| `path` | Percorso del parametro da aggiornare. |
| `value` | Il nuovo valore con cui desideri aggiornare il parametro. |

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli aggiornati dell&#39;offerta di fallback, inclusa l&#39;istanza univoca `id`.

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
