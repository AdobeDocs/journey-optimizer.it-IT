---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Aggiornare le offerte personalizzate
description: Un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.
feature: Decision Management, API
badge: label="Legacy" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: 9d8f2df6-aa04-4e66-8555-d51c2e409063
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/eqK42y-xkg200RV-mPy826hg3uD6W6PO2mTNGQkTjfg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 20%

---

# Aggiornare un’offerta personalizzata {#update-personalized-offer}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../../../experience-decisioning/gs-experience-decisioning.md)


È possibile modificare o aggiornare un&#39;offerta personalizzata effettuando una richiesta PATCH all&#39;API [!DNL Offer Library]

Per ulteriori informazioni sulla patch JSON, incluse le operazioni disponibili, consulta la [documentazione ufficiale sulla patch JSON](https://jsonpatch.com/).

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che costituiscono il campo *Content-Type* nell&#39;intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato API**

```http
PATCH /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API di persistenza. | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID dell’entità da aggiornare. | `personalizedOffer1234` |

**Richiesta**

```shell
curl -X PATCH 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '[
    {
        "op": "replace",
        "path": "/name",
        "value": "Updated personalized offer"
    },
    {
        "op": "replace",
        "path": "/description",
        "value": "Updated personalized offer description"
    }
]'
```

| Parametro | Descrizione |
| --------- | ----------- |
| `op` | Chiamata di operazione utilizzata per definire l&#39;azione necessaria per aggiornare la connessione. Le operazioni includono: `add`, `replace`, `remove`, `copy` e `test`. |
| `path` | Percorso del parametro da aggiornare. |
| `value` | Il nuovo valore con cui desideri aggiornare il parametro. |

**Risposta**

In caso di esito positivo, la risposta restituisce i dettagli aggiornati del posizionamento, incluso l’ID posizionamento.

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
