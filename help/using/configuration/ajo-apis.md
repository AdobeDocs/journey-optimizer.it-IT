---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare le API di Journey Optimizer
description: Journey Optimizer fornisce API RESTful che consentono di eseguire in modo programmatico operazioni chiave nelle applicazioni. Scopri come accedervi e utilizzarli.
feature: Integrations, Data Ingestion
role: Developer
level: Intermediate
exl-id: 4c897c52-6eb2-4d6e-aaa9-9bd83608b2b6
source-git-commit: cbfebeaaa3ef6e55d48457012fd94bd74afc91de
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 4%

---

# Utilizzare le API [!DNL Journey Optimizer] {#apis-gs}

## Accesso rapido {#quick-access}

>[!IMPORTANT]
>
>**Introduzione alle API di Journey Optimizer:**
>
>* **[Sfoglia il riferimento API completo](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"}** - Accedi a tutte le API Journey Optimizer e testale direttamente
>* **[Configura autenticazione](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"}** - Raccogli le credenziali richieste per iniziare a utilizzare le API
>* **[API di gestione delle decisioni](../offers/api-reference/getting-started.md)** - Gestire le offerte e le decisioni a livello di programmazione
>* **[API Experience Decisioning](../experience-decisioning/api-reference/deliver.md)** - Distribuisci elementi decisionali personalizzati utilizzando esperienze basate su codice

## Panoramica {#overview}

L’API di Adobe Journey Optimizer ti consente di fornire esperienze cliente personalizzate, connesse e tempestive su qualsiasi app, dispositivo o canale e, a sua volta, di gestire efficacemente il percorso cliente end-to-end. Per percorso di clienti si intende l’intero processo di interazione del cliente con un marchio, dal primo contatto fino a quando il cliente se ne va. Inizia con la fase di consapevolezza, in cui il cliente viene a conoscenza del marchio e inizia a essere coinvolto. Il cliente interagirà ulteriormente con il marchio, visiterà siti online e fisici, effettuerà acquisti, invierà messaggi o pubblicherà recensioni.

Adobe Journey Optimizer è stato sviluppato in modalità nativa su Adobe Experience Platform e combina un profilo cliente unificato e in tempo reale, un framework aperto API-first, offer decisioning centralizzato, nonché intelligenza artificiale (IA) e machine learning (ML) per la personalizzazione e l’ottimizzazione. Integrandosi con l’API di Journey Optimizer, i brand possono determinare in modo intelligente la migliore interazione successiva con scalabilità, velocità e flessibilità nell’intero percorso di clienti.

## Autenticazione {#authentication}

Prima di utilizzare le API di Journey Optimizer, è necessario impostare l’autenticazione per accedere agli endpoint API.

Segui la [guida all&#39;autenticazione](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} per raccogliere le credenziali di autenticazione richieste per tutte le API di Journey Optimizer.

## Documentazione API {#api-documentation}

La documentazione API completa di Adobe Journey Optimizer include informazioni dettagliate su tutti gli endpoint disponibili, i formati di richiesta/risposta e le funzionalità di test interattivo.

Accedi alla [documentazione API di Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/){target="_blank"} e sfoglia il menu **Riferimenti API** per esplorare tutte le API disponibili.

## API di gestione delle decisioni {#decision-management-apis}

Journey Optimizer fornisce API dedicate per la gestione delle decisioni, che consentono di gestire in modo programmatico offerte, decisioni e posizionamenti.

Per iniziare a utilizzare le API di Offer Decisioning, consulta la [Guida per gli sviluppatori API per la gestione delle decisioni](../offers/api-reference/getting-started.md).

## API di Experience Decisioning {#experience-decisioning-apis}

Journey Optimizer offre anche API Experience Decisioning per la distribuzione di elementi decisionali personalizzati tramite esperienze basate su codice. Experience Decisioning offre un approccio semplificato alla personalizzazione con elementi decisionali, regole di idoneità e strategie di selezione.

**Operazioni API disponibili:**

* **Elementi decisionali** - Crea, leggi, aggiorna ed elimina elementi decisionali
* **Strategie di selezione** - Definisci come selezionare e classificare gli elementi decisionali
* **Regole di idoneità** - Imposta le condizioni per l&#39;idoneità degli elementi
* **Raccolte elementi** - Organizza gli elementi decisionali in raccolte
* **Formule di classificazione** - Configura logica di classificazione personalizzata
* **Posizionamenti** - Definisci dove possono comparire gli elementi decisionali

Ulteriori informazioni sono disponibili in [Riferimento API di Experience Decisioning](../experience-decisioning/api-reference/deliver.md) e scopri come [distribuire offerte utilizzando esperienze basate su codice](../experience-decisioning/api-reference/deliver.md).
