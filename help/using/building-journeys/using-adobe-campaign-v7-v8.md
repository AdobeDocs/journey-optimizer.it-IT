---
solution: Journey Optimizer
product: journey optimizer
title: Azioni Adobe Campaign v7/v8
description: Scopri le azioni di Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: percorso, integrazione, campagna, v7, v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
version: Journey Orchestration
source-git-commit: a068d3a4005d8f2247755f56ffb70665dc4c957f
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 25%

---

# Azioni Adobe Campaign v7/v8 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Azioni personalizzate"
>abstract="Se si dispone di Adobe Campaign v7 o v8, è disponibile un’integrazione. Consente di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign."

Se si dispone di Adobe Campaign v7 o v8, è disponibile un’integrazione. Consente di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign.

La connessione tra le istanze Journey Optimizer e Campaign viene impostata da Adobe al momento del provisioning. Contatta Adobe.

**Quando utilizzare**: utilizza le azioni di Campaign v7/v8 quando la messaggistica si basa su modelli transazionali di Campaign, modelli di dati specifici di Campaign o flussi di lavoro di consegna di Campaign esistenti.

**Prerequisiti**

* L’istanza di Adobe Campaign v7/v8 dispone del provisioning e è connessa a Journey Optimizer da Adobe.
* Hai accesso alla messaggistica transazionale di Campaign e alle autorizzazioni necessarie.

Affinché questo funzioni, devi configurare un’azione dedicata. Consulta questa [sezione](../action/acc-action.md).

Un caso d&#39;uso end-to-end è presentato in questa [sezione](../building-journeys/ajo-ac.md).

1. Progetta il percorso, a partire da un evento. Consulta questa [sezione](../building-journeys/journey.md).
1. Nella sezione **Azione** della palette, seleziona un&#39;azione Campaign e aggiungila al percorso.
1. Nei **Parametri azione**, vengono visualizzati tutti i campi previsti nel payload del messaggio. Devi mappare ciascuno di questi campi con il campo che desideri utilizzare, dall’evento o dall’origine dati. È simile alle azioni personalizzate. Consulta questa [sezione](../building-journeys/using-custom-actions.md).

>[!NOTE]
>
>* Le azioni di Campaign v7/v8 possono essere utilizzate insieme alle azioni del canale nativo nello stesso percorso. Questo non si applica alle azioni di Campaign Standard. Consulta [Guardrail attività campagna](../start/guardrails.md#ac-g).
>* Le azioni di Campaign v7/v8 non possono essere utilizzate con le attività Read Audience o Audience Qualification. Consulta i guardrail Read Audience and Audience Qualification nella pagina Guardrail.

![Impostazioni di integrazione e configurazione azioni di Adobe Campaign v7/v8](assets/accintegration2.png)
