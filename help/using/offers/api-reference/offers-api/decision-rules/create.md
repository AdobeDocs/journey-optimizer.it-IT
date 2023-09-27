---
title: Creare una regola di decisione
description: Le regole di decisione sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 6a05efca-31bd-46d5-998d-ff3038d9013f
source-git-commit: 805f7bdc921c53f63367041afbb6198d0ec05ad8
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 13%

---

# Creare una regola di decisione {#create-decision-rule}

Le regole di decisione sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

La tabella seguente mostra i valori validi che compongono *Content-Type* nell’intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Content-Type | `application/json` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/offer-rules
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso dell’endpoint per le API dell’archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le regole di decisione. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Richiesta**

```shell
curl -X POST 'https://platform.adobe.io/data/core/dps/offer-rules' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-d '{
    "name": "Sales rule",
    "description": "Decisioning rule for sales",
    "condition": {
        "type": "PQL",
        "format": "pql/text",
        "value": "profile.person.name.firstName.equals(\"Joe\", false)"
    },
    "definedOn": {
        "profile": {
            "schema": {
                "ref": "https://ns.adobe.com/xdm/context/profile_union",
                "version": "1"
            },
            "referencePaths": [
                "person.name.firstName"
            ]
        }
    }
}'
```

**Risposta**

In caso di esito positivo, la risposta restituisce informazioni sulla regola di decisione appena creata, incluso il posizionamento `id`. È possibile utilizzare `id` nei passaggi successivi per aggiornare o eliminare la regola di decisione o utilizzarla in un tutorial successivo per creare decisioni, regole di decisione e offerte di fallback.

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
