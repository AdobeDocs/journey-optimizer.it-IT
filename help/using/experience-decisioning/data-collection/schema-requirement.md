---
solution: Journey Optimizer
product: Journey Optimizer
title: Configurare l’acquisizione di eventi
description: Scopri come configurare lo schema di offerta per acquisire gli eventi
feature: Ranking, Datasets, Decisioning
role: Developer
level: Experienced
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 1%

---

# Configurare la raccolta dati {#schema-requirements}

Per ottenere un feedback su tipi di evento diversi dagli eventi di decisione, è necessario impostare il valore corretto per ciascun tipo di evento in un **evento esperienza** inviato in Adobe Experience Platform.

>[!CAUTION]
>
>Per ogni tipo di evento, accertati che allo schema utilizzato nel set di dati sia associato il gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposta]**. <!--[Learn more](create-dataset.md)-->

Di seguito sono riportati i requisiti dello schema da implementare nel codice JavaScript.

## Tracciare le impression {#track-impressions}

Assicurati che i seguenti campi siano configurati correttamente:

**Tipo di evento esperienza:** `decisioning.propositionDisplay`

**propositionEventType:** `_experience.decisioning.propositionEventType.display`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o acquisizione batch

+++**Payload di esempio:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "display": 1
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionDisplay",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b219",
  "timestamp": "2025-10-07T20:22:00Z"
}
```

+++

## Tracciare i clic {#track-clicks}

Assicurati che i seguenti campi siano configurati correttamente:

**Tipo di evento esperienza:** `decisioning.propositionInteract`

**propositionEventType:** `_experience.decisioning.propositionEventType.interact`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o acquisizione batch

Ogni offerta all’interno di una proposta include un token di tracciamento, che è un identificatore univoco generato da Adobe. Questo token deve essere trasmesso esattamente come ricevuto, senza modifiche, nell’evento di clic o impression corrispondente. La corrispondenza dei token di tracciamento garantisce che Adobe possa associare con precisione l’azione dell’utente alla decisione di offerta corretta, abilitando il reporting a valle e l’ottimizzazione basata sull’intelligenza artificiale.

>[!CAUTION]
>
>Se non si passa il token di tracciamento nel campo `propositionAction.tokens` durante il tracciamento dei clic, gli eventi di clic non verranno attribuiti correttamente all&#39;offerta corrispondente. Questo comporterà dati di tracciamento incompleti e avrà un impatto negativo sul reporting e sull’ottimizzazione del ranking basata sull’intelligenza artificiale. Accertati sempre di includere il token di tracciamento della proposta nell’implementazione del tracciamento dei clic.

+++**Payload di esempio:**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "interact": 1
      },
      "propositionAction": {
        "tokens": [
          "Vx9fwWXmp6/kyYRVOUZWEQ"
        ]
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionInteract",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b765",
  "timestamp": "2025-10-07T20:50:00Z"
}
```

+++

## Tracciare eventi personalizzati {#track-custom-events}

Per gli eventi personalizzati, allo schema utilizzato nel set di dati deve essere associato anche il gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposta]**, ma non esiste alcun requisito specifico per il tipo di evento esperienza che deve essere utilizzato per assegnare tag a tali eventi.

<!--

>[!NOTE]
>
>To have your custom events accounted for in [capping](../items.md#capping), you need to connect the experience event to Adobe Experience Platform endpoints by sending it to either one of these two Edge data collection endpoints:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>If you are using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=it){target="_blank"}, the connection is made automatically.-->
