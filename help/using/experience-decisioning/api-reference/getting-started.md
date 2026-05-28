---
title: Introduzione alle API Decisioning
description: Scopri come iniziare a utilizzare le API Decisioning per gestire in modo programmatico gli elementi decisionali e distribuire offerte personalizzate.
feature: API, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 78ed06a3-7787-4aab-8373-df7eb40c1727
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/01NgEXGvNxeb1MNkjeB55VNFZFuSiTfQMKeNahfuHWE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 339
ht-degree: 5%

---

# Guida per gli sviluppatori API Decisioning {#decisioning-api-developer-guide}

Le API Decisioning ti consentono di creare e gestire in modo programmatico i componenti utilizzati per distribuire offerte personalizzate ai clienti. Queste API RESTful forniscono operazioni CRUD (Create, Read, Update, Delete) complete per elementi decisionali, strategie di selezione, regole di idoneità e altri componenti decisionali.

## Autenticazione {#authentication}

Prima di utilizzare le API Decisioning, è necessario impostare l’autenticazione per accedere agli endpoint API. Per istruzioni dettagliate, consulta la [guida all&#39;autenticazione di Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/authentication){target="_blank"}.

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

>[!NOTE]
>
>Se devi eseguire la migrazione degli oggetti di gestione delle decisioni esistenti in Decisioning, utilizza l&#39;[API di migrazione Decisioning](../decisioning-migration-api.md) dedicata. Questa API specializzata fornisce funzionalità automatizzate di risoluzione e rollback delle dipendenze progettate appositamente per la migrazione delle entità decisionali tra sandbox diverse.
