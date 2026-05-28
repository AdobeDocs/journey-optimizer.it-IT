---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Configurare l’acquisizione di eventi
description: Scopri come configurare lo schema di offerta per acquisire gli eventi
badge: label="Legacy" type="Informative"
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/DhaXO7sS2zR9iewgoQjrN5ptYNpYSt97e-hflU2iq7c
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2id: ad78185d-8f79-40ad-9bad-cbde74af74ee
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 10%

---

# Configurare la raccolta dati {#schema-requirements}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)

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
>Affinché gli eventi personalizzati vengano contabilizzati in [quota limite](../offer-library/add-constraints.md#capping), è necessario collegare l&#39;evento esperienza agli endpoint Adobe Experience Platform inviandolo a uno dei due endpoint di raccolta dati Edge seguenti:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Se si utilizza [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it){target="_blank"} o [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}, la connessione viene stabilita automaticamente.
