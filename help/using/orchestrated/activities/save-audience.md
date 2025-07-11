---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Save audience
description: Scopri come utilizzare l’attività Save audience in una campagna orchestrata
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 7b5b03ba-fbb1-4916-8c72-10778752d8e4
source-git-commit: 779c90f0be57749a63da103d18cc642106c5f837
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 8%

---

# Salva pubblico {#save-audience}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](../configuration-steps.md)<br/><br/>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](and-join.md) - [Genera pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - <b>[Salva pubblico](save-audience.md)</b> - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

Documentazione in corso

>[!ENDSHADEBOX]

L&#39;attività **[!UICONTROL Save audience]** è un&#39;attività **[!UICONTROL Targeting]** che consente di aggiornare un pubblico esistente o crearne uno nuovo dalla popolazione generata in precedenza nella campagna orchestrata. Una volta creati, questi tipi di pubblico vengono aggiunti all&#39;elenco dei tipi di pubblico dell&#39;applicazione e sono accessibili dal menu **[!UICONTROL Tipi di pubblico]**.

Questa attività è particolarmente utile per mantenere i segmenti di pubblico calcolati all’interno della stessa campagna orchestrata, rendendoli disponibili per il riutilizzo in campagne future. In genere è connesso ad altre attività di targeting, come **[!UICONTROL Genera pubblico]** o **[!UICONTROL Combina]**, per acquisire e salvare la popolazione risultante.

## Configurare l’attività Salva pubblico {#save-audience-configuration}

Per configurare l’attività **[!UICONTROL Salva pubblico]**, segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Save audience]** alla campagna orchestrata.

1. Immetti una **[!UICONTROL etichetta di pubblico]** che identificherà il pubblico salvato.

1. Fai clic su **[!UICONTROL Aggiungi attributo pubblico]** per definire la struttura e la memorizzazione dei dati sul pubblico da riutilizzare in futuro.

   ![](../assets/save-audience-1.png)

1. Quindi, seleziona il **[!UICONTROL campo di identità primaria]** &#x200B;e il **[!UICONTROL spazio dei nomi di identità]** appropriati per garantire una risoluzione accurata del profilo.

   ![](../assets/save-audience-2.png)

1. Completa la configurazione salvando e pubblicando la campagna orchestrata. Questo genererà e memorizzerà il tuo pubblico.

Il contenuto del pubblico salvato è quindi disponibile nella relativa visualizzazione dettagliata, accessibile dal menu **[!UICONTROL Tipi di pubblico]**.

![](../assets/save-audience-3.png)

## Esempio {#save-audience-example}

L’esempio seguente illustra come creare un pubblico semplice utilizzando il targeting. Una query identifica tutti i profili che hanno effettuato un acquisto negli ultimi 30 giorni. L&#39;attività **[!UICONTROL Save audience]** acquisisce quindi questi profili per creare un pubblico riutilizzabile di acquirenti recenti.

![](../assets/save-audience-4.png)
