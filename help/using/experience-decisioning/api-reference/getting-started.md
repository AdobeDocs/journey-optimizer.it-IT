---
title: Introduzione alle API Decisioning
description: Scopri come iniziare a utilizzare le API Decisioning per gestire in modo programmatico gli elementi decisionali e distribuire offerte personalizzate.
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7a4b5d4e-9c1d-4f3a-b8e9-1d5f6e7a8c3a
version: Journey Orchestration
source-git-commit: e46ab0637a0fa4a2b4b8b6ff3b8ab3eb5d38e0f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 4%

---

# Guida per gli sviluppatori API Decisioning {#decisioning-api-developer-guide}

Le API Decisioning ti consentono di creare e gestire in modo programmatico i componenti utilizzati per distribuire offerte personalizzate ai clienti. Queste API RESTful forniscono operazioni CRUD (Create, Read, Update, Delete) complete per elementi decisionali, strategie di selezione, regole di idoneità e altri componenti decisionali.

## Autenticazione {#authentication}

Prima di utilizzare le API Decisioning, è necessario impostare l’autenticazione per accedere agli endpoint API. Per istruzioni dettagliate, consulta la [guida all&#39;autenticazione di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}.

## Operazioni API disponibili {#available-operations}

Le API Decisioning forniscono funzionalità di gestione complete per i componenti decisioning. Sono disponibili le seguenti categorie di operazioni:

* **Elementi decisionali** - Crea, leggi, aggiorna, elimina ed elenca gli elementi decisionali che rappresentano le offerte o i contenuti che desideri consegnare ai clienti.

  ➡️ [Scopri come gestire gli elementi decisionali](decisions-items/create.md)

* **Raccolte di elementi** - Organizza gli elementi decisionali in raccolte per semplificarne la gestione e il targeting utilizzando le regole di idoneità.

  ➡️ [Scopri come gestire le raccolte di elementi](items-collections/create.md)

* **Strategie di selezione** - Definisci come vengono selezionati e classificati gli elementi decisionali quando più elementi sono idonei per la consegna.

  ➡️ [Scopri come gestire le strategie di selezione](selection-strategies/create.md)

* **Regole di idoneità** - Imposta le condizioni che determinano quali profili sono idonei a ricevere elementi decisionali specifici.

  ➡️ [Scopri come gestire le regole di idoneità](eligibility-rules/create.md)

* **Formule di classificazione** - Crea una logica di classificazione personalizzata per determinare l&#39;ordine in cui vengono presentati gli elementi decisionali.

  ➡️ [Scopri come gestire le formule di classificazione](ranking-formulas/create.md)

* **Posizionamenti** - Definisci le posizioni o i contesti in cui gli elementi decisionali possono essere visualizzati nelle esperienze.

  ➡️ [Scopri come gestire i posizionamenti](exd-placements/create.md)

## Passaggi successivi {#next-steps}

Ora che conosci le nozioni di base delle API Decisioning, puoi procedere alle operazioni specifiche:

* [Creare elementi decisionali](decisions-items/create.md)
* [Elencare elementi decisionali](decisions-items/decision-items-list.md)
* [Creare strategie di selezione](selection-strategies/create.md)
* [Creare regole di idoneità](eligibility-rules/create.md)

Per ulteriori informazioni sull&#39;utilizzo del decisioning nelle campagne e nei percorsi, consulta la [documentazione sul decisioning](../gs-experience-decisioning.md).
