---
product: experience platform
solution: Experience Platform
title: Configurare l’acquisizione di eventi
description: Scopri come configurare lo schema di offerta per acquisire gli eventi
feature: Ranking Formulas, Datasets, Offers
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 5%

---

# Configurare la raccolta dati {#schema-requirements}

Per poter ottenere feedback su tipi di evento diversi dagli eventi di decisione, è necessario impostare il valore corretto per ciascun tipo di evento in un **evento esperienza** inviato a Adobe Experience Platform.

>[!CAUTION]
>
>Per ogni tipo di evento, assicurati che lo schema utilizzato nel set di dati abbia **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi ad esso associato. [Ulteriori informazioni](create-dataset.md)

Di seguito sono riportati i requisiti dello schema da implementare nel codice JavaScript.

>[!NOTE]
>
>Non è necessario inviare gli eventi di decisione, in quanto la gestione delle decisioni genererà tali eventi automaticamente e li inserirà nel **[!UICONTROL ODE DecisionEvents]** set di dati<!--to check--> generato automaticamente.

## Tracciare le impression {#track-impressions}

Assicurati che il tipo di evento e l’origine siano i seguenti:

**Tipo di evento esperienza:** `decisioning.propositionDisplay`
**Origine:** Web.sdk/Alloy.js`sendEvent command -> xdm : {eventType, interactionMixin}`) o acquisizione batch
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

## Tracciare i clic {#track-clicks}

Assicurati che il tipo di evento e l’origine siano i seguenti:

**Tipo di evento esperienza:** `decisioning.propositionInteract`
**Origine:** Web.sdk/Alloy.js`sendEvent command -> xdm : {eventType, interactionMixin}`) o acquisizione batch
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

## Tracciare eventi personalizzati {#track-custom-events}

Per gli eventi personalizzati, lo schema utilizzato nel set di dati deve avere anche **[!UICONTROL Evento esperienza - Interazioni proposte]** gruppo di campi ad esso associato, ma non esiste alcun requisito specifico sul tipo di evento esperienza che deve essere utilizzato per assegnare tag a tali eventi.

>[!NOTE]
>
>Per poter contabilizzare gli eventi personalizzati in [quota limite](../offer-library/add-constraints.md#capping), è necessario collegare l’evento esperienza agli endpoint Adobe Experience Platform inviandolo a uno dei due endpoint di raccolta dati Edge:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Se utilizzi il [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}, la connessione viene effettuata automaticamente.
