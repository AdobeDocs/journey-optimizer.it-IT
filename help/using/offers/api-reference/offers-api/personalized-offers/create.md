---
title: Creare le offerte personalizzate
description: Un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 97dc9af3-ca31-4512-aad2-f959dfc9ad0b
source-git-commit: bdb7b6373cb9f5a64a74a8503f46adb3fd226f77
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Creare un’offerta personalizzata {#create-personalized-offer}

Un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.

Puoi creare un’offerta personalizzata effettuando una richiesta di POST al [!DNL Offer Library] , fornendo al tempo stesso l&#39;ID del contenitore.

## Intestazioni Accept e Content-Type {#accept-and-content-type-headers}

Nella tabella seguente sono riportati i valori validi che comprendono *Content-Type* e *Accetta* campi nell’intestazione della richiesta:

| Nome intestazione | Valore |
| ----------- | ----- |
| Accept | `application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1` |
| Content-Type | `application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"` |

**Formato API**

```http
POST /{ENDPOINT_PATH}/{CONTAINER_ID}/instances
```

| Parametro | Descrizione | Esempio |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Percorso endpoint per le API dell&#39;archivio. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Il contenitore in cui si trovano le offerte personalizzate. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |

**Richiesta**

```shell
curl -X POST \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Content-Type: application/schema-instance+json; version=1;  schema="https://ns.adobe.com/experience/offer-management/personalized-offer;version=0.5"' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}' \
  -d '{
        "xdm:name": "Sale offer",
        "xdm:status": "draft",
        "xdm:representations": [
            {
                "xdm:components": [
                    {
                        "dc:language": [
                            "en"
                        ],
                        "@type": "https://ns.adobe.com/experience/offer-management/content-component-html",
                        "dc:format": "text/html"
                    }
                ],
                "xdm:placement": "xcore:offer-placement:124e0be5699743d3"
            }
        ],
        "xdm:selectionConstraint": {
            "xdm:startDate": "2020-10-01T16:00:00Z",
            "xdm:endDate": "2021-12-13T16:00:00Z",
            "xdm:eligibilityRule": "xcore:eligibility-rule:124e0faf5b8ee89b"
        },
        "xdm:rank": {
            "xdm:priority": 1
        },
        "xdm:cappingConstraint": {
            "xdm:globalCap": 150
        },
        "xdm:tags": [
            "xcore:tag:124e147572cd7866"
        ]
    }'
```

**Risposta**

Una risposta corretta restituisce informazioni sull’offerta personalizzata appena creata, incluso l’ID istanza univoco e il posizionamento `@id`. Puoi utilizzare l’ID istanza nei passaggi successivi per aggiornare o eliminare l’offerta personalizzata.

```json
{
    "instanceId": "0f4bc230-13df-11eb-bc55-c11be7252432",
    "@id": "xcore:personalized-offer:124e181c8b0d7878",
    "repo:etag": 1,
    "repo:createdDate": "2020-10-21T20:50:32.018624Z",
    "repo:lastModifiedDate": "2020-10-21T20:50:32.018624Z",
    "repo:createdBy": "{CREATED_BY}",
    "repo:lastModifiedBy": "{MODIFIED_BY}",
    "repo:createdByClientId": "{CREATED_CLIENT_ID}",
    "repo:lastModifiedByClientId": "{MODIFIED_CLIENT_ID}"
}
```

## Limitazioni  {#limitations}

Le rappresentazioni delle offerte e alcuni vincoli di offerta non sono attualmente supportati con il dispositivo mobile [!DNL Experience Edge] flussi di lavoro, ad esempio `Capping`. La `Capping` il valore campo specifica il numero di volte in cui un’offerta può essere presentata in tutti gli utenti. Per ulteriori dettagli, consulta [Documentazione sulle regole di idoneità e sui vincoli delle offerte](../../../offer-library/creating-personalized-offers.md).