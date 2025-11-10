---
product: experience platform
solution: Experience Platform
title: Richieste di dati contestuali e decisioning
description: Scopri come trasmettere i dati contestuali nelle richieste Decisioning.
badge: label="Legacy" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 45d060ce-0a12-4a6e-a594-ec10cdff8f38
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Richieste di dati contestuali e decisioning {#context-data-decisioning}

Questa sezione ti guida attraverso il passaggio di dati contestuali nelle richieste Decisioning e il loro utilizzo nelle regole di idoneità.

>[!BEGINSHADEBOX]

Per andare oltre, puoi anche sfruttare il contesto nelle **formule di classificazione** per aumentare le offerte. Esempi dettagliati di formule di classificazione che sfruttano i dati contestuali sono disponibili in [questa sezione](../offers/ranking/create-ranking-formulas.md#context-data).

>[!ENDSHADEBOX]

## Trasmettere i dati contestuali nelle richieste Decisioning

I dati contestuali nelle richieste Decisioning sono definiti utilizzando la chiave: `xdm:ContextData`.

Gli attributi dei dati contestuali non sono guidati dallo schema XDM. Puoi trasmettere qualsiasi dato contestuale in JSON come parte del payload della richiesta Decisioning.

Di seguito è riportato un esempio di richiesta di decisioni con dati contestuali (vedere `xdm:ContextData`):

```
curl --location 'https://platform-stage.adobe.io/data/core/ods/decisions' \
--header 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
--header 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
--header 'Authorization: Bearer eyJhbGciOi....' \
--header 'x-api-key: {{api_key}}' \
--header 'x-gw-ims-org-id: {{ims_org}}' \
--header 'x-sandbox-name: {{sandbox_name}}' \
--header 'x-request-id: {{$guid}}' \
--data-raw '{
    "xdm:propositionRequests": [
        {
            "xdm:activityId": "dps:offer-activity:19978bf95ebfc8fb",
            "xdm:placementId": "dps:offer-placement:199772e1c90d50ac"
        }
    ],
    "xdm:profiles": [
        {
            "xdm:identityMap": {
                "Email": [
                    {
                        "xdm:id": "test@test.com",
                        "primary": true
                    }
                ]
            },
            "xdm:contextData": [
                {
                    "@type": "_xdm.context.additionalParameters;version=1",
                    "xdm:data": {
                        "xdm:channel": "mobile",
                        "xdm:language": "en",
                        "xdm:isThirdParty": true,
                        "xdm:mobileVersion": "3.0.5106",
                        "xdm:mobileVersionMajor": "3",
                        "xdm:mobileVersionMinor": "0",
                        "xdm:mobileVersionPatch": "125",
                        "xdm:deviceType": "iOS",
                        "xdm:features": [
                            "p1000",
                            "p1001"
                        ]
                    }
                }
            ]
        }
    ],
    "xdm:allowDuplicatePropositions": {
        "xdm:acrossActivities": true,
        "xdm:acrossPlacements": true
    },
    "xdm:responseFormat": {
        "xdm:includeContent": true,
        "xdm:includeMetadata": {
            "xdm:activity": [
                "name"
            ],
            "xdm:option": [
                "name"
            ],
            "xdm:placement": [
                "name"
            ]
        }
    }
}'
```

## Utilizzare i dati contestuali nelle regole di idoneità

Di seguito sono riportati alcuni esempi che illustrano come utilizzare i dati contestuali passati nelle richieste Decisioning nelle regole di idoneità.

* Idoneo se le funzioni dei dati contestuali contengono un valore particolare:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where contextData.features AND (select personetic from contextData.features where personetic.contains("123"))
  ```

* Idoneo se il canale non è vuoto e corrisponde a mobile:

  ```
  select contextData from @{_xdm.context.additionalParameters;version=1} where !contextData.channel.isNull() AND contextData.channel!="" AND contextData.channel="mobile"
  ```
