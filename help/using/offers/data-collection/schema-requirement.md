---
product: experience platform
solution: Experience Platform
title: Configurare l’acquisizione di eventi
description: Scopri come configurare lo schema dell’offerta per l’acquisizione di eventi
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 2%

---

# Configurare la raccolta dati {#schema-requirements}

<!--To send in feedback data, you must define how the experience events will be captured.-->

Per ottenere un feedback su tipi di evento diversi dagli eventi decisionali, è necessario impostare il valore corretto per ogni tipo di evento in un **evento esperienza** viene inviato in Adobe Experience Platform.

Per ogni tipo di evento, assicurati che lo schema utilizzato nel set di dati disponga della **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi associato. [Ulteriori informazioni](create-dataset.md)

Di seguito sono riportati i requisiti dello schema da implementare nel codice JavaScript.

>[!NOTE]
>
>Gli eventi decisionali non devono essere inviati in quanto la gestione delle decisioni genererà automaticamente tali eventi e li inserirà nel **[!UICONTROL Decisioni ODE]** set di dati<!--to check--> generato automaticamente.

## Tracciare le impression

Assicurati che il tipo di evento e l&#39;origine siano i seguenti:

**Tipo di evento esperienza:** `decisioning.propositionDisplay`
**Origine:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o acquisizione batch
+++**Payload di esempio:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for "nextBestOffer"
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for "nextBestOffer"
        }
    ]
}
```

+++

## Tracciare i clic

Assicurati che il tipo di evento e l&#39;origine siano i seguenti:

**Tipo di evento esperienza:** `decisioning.propositionInteract`
**Origine:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o acquisizione batch
+++**Payload di esempio:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

## Tracciare gli eventi personalizzati

Per gli eventi personalizzati, lo schema utilizzato nel set di dati deve avere anche il **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi ad esso associato, ma non esiste un requisito specifico per il tipo di evento esperienza che deve essere utilizzato per assegnare tag a tali eventi.

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->
