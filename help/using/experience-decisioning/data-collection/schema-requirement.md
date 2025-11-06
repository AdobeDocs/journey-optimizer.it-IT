---
product: experience platform
solution: Experience Platform
title: Configurare l’acquisizione di eventi
description: Scopri come configurare lo schema di offerta per acquisire gli eventi
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
hide: true
hidefromtoc: true
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---

# Configurare la raccolta dati {#schema-requirements}

Per ottenere un feedback su tipi di evento diversi dagli eventi di decisione, è necessario impostare il valore corretto per ciascun tipo di evento in un **evento esperienza** inviato in Adobe Experience Platform.

>[!CAUTION]
>
>Per ogni tipo di evento, accertati che allo schema utilizzato nel set di dati sia associato il gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposta]**. [Ulteriori informazioni](create-dataset.md)

Di seguito sono riportati i requisiti dello schema da implementare nel codice JavaScript.

>[!NOTE]
>
>Non è necessario inviare gli eventi di decisione perché verranno generati automaticamente e inseriti nel set di dati **[!UICONTROL ODE DecisionEvents]**<!--to check--> generato automaticamente.

## Tracciare le impression {#track-impressions}

Assicurati che il tipo di evento e l’origine siano i seguenti:

**Tipo di evento esperienza:** `decisioning.propositionDisplay`
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o acquisizione batch
+++**Payload di esempio:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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
**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) o acquisizione batch
+++**Payload di esempio:**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

Per gli eventi personalizzati, allo schema utilizzato nel set di dati deve essere associato anche il gruppo di campi **[!UICONTROL Evento esperienza - Interazioni proposta]**, ma non esiste alcun requisito specifico per il tipo di evento esperienza che deve essere utilizzato per assegnare tag a tali eventi.

>[!NOTE]
>
>Affinché gli eventi personalizzati vengano inclusi nel [limite](../items.md#capping), è necessario connettere l&#39;evento esperienza agli endpoint Adobe Experience Platform inviandolo a uno dei due endpoint di raccolta dati di Edge:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Se si utilizza [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it){target="_blank"} o [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=it){target="_blank"}, la connessione viene stabilita automaticamente.
