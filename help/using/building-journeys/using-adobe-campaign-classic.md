---
solution: Journey Optimizer
product: journey optimizer
title: Azioni Adobe Campaign v7/v8
description: Scopri le azioni di Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
keywords: percorso, integrazione, campagna, v7, v8, classico
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 13%

---

# Azioni Adobe Campaign v7/v8 {#using_campaign_classic}

Se si dispone di Adobe Campaign v7 o v8, è disponibile un’integrazione. Ti consentirà di inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign.

La connessione tra le istanze Journey Optimizer e Campaign viene impostata per Adobe al momento del provisioning. Adobe di contatto.

Affinché questo funzioni, devi configurare un’azione dedicata. Fai riferimento a questo [sezione](../action/acc-action.md).

In questo viene presentato un caso d’uso end-to-end [sezione](../building-journeys/ajo-ac.md).

1. Progetta il tuo percorso, a partire da un evento. Vedi questo [sezione](../building-journeys/journey.md).
1. In **Azione** nella sezione della palette, seleziona un’azione Campaign e aggiungilo al percorso.
1. In **Parametri azione**, vengono visualizzati tutti i campi previsti nel payload del messaggio. Devi mappare ciascuno di questi campi con il campo che desideri utilizzare, dall’evento o dall’origine dati. È simile alle azioni personalizzate. Fai riferimento a questo [sezione](../building-journeys/using-custom-actions.md).

![](assets/accintegration2.png)
