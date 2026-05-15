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
TQID: https://experienceleague.adobe.com/Saqu6Kkm1Rdym10IuwLF88Fj-hT2crAwENajyKBeY5w
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 28%

---

# Azioni di [!DNL Adobe Campaign] v7/v8 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Azioni personalizzate"
>abstract="È disponibile un’integrazione per [!DNL Adobe Campaign] v7 o v8. Consente di inviare e-mail, notifiche push ed SMS utilizzando le funzionalità di messaggistica transazionale di [!DNL Adobe Campaign]."

È disponibile un’integrazione per [!DNL Adobe Campaign] v7 o v8. Consente di inviare e-mail, notifiche push ed SMS utilizzando le funzionalità di messaggistica transazionale di [!DNL Adobe Campaign].

La connessione tra le istanze di Journey Optimizer e Campaign viene impostata da Adobe al momento del provisioning. Contatta Adobe.

**Quando utilizzare**: utilizza le azioni di Campaign v7/v8 quando la messaggistica si basa su modelli transazionali di Campaign, modelli di dati specifici di Campaign o flussi di lavoro di consegna di Campaign esistenti.

**Prerequisiti**

* L&#39;istanza di [!DNL Adobe Campaign] v7/v8 è stata predisposta e connessa a Journey Optimizer da Adobe.
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

Impostazioni di integrazione e configurazione delle azioni ![[!DNL Adobe Campaign] v7/v8](assets/accintegration2.png)
