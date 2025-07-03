---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Save audience
description: Scopri come utilizzare l’attività Save audience in una campagna orchestrata
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 16%

---

# Salva pubblico {#save-audience}

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Accedere e gestire le campagne orchestrate](access-manage-orchestrated-campaigns.md) | [Passaggi chiave per la creazione orchestrata della campagna](gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/><b>[Avviare e monitorare la campagna](start-monitor-campaigns.md)</b><br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

L&#39;attività **[!UICONTROL Save audience]** è un&#39;attività **[!UICONTROL Targeting]** che consente di aggiornare un pubblico esistente o crearne uno nuovo dalla popolazione generata in precedenza nella campagna orchestrata. Una volta creati, questi tipi di pubblico vengono aggiunti all&#39;elenco dei tipi di pubblico dell&#39;applicazione e sono accessibili dal menu **[!UICONTROL Tipi di pubblico]**.

Questa attività è particolarmente utile per mantenere i segmenti di pubblico calcolati all’interno della stessa campagna orchestrata, rendendoli disponibili per il riutilizzo in campagne future. In genere è connesso ad altre attività di targeting, come **[!UICONTROL Genera pubblico]** o **[!UICONTROL Combina]**, per acquisire e salvare la popolazione risultante.

## Configurare l’attività Salva pubblico {#save-audience-configuration}

Per configurare l’attività **Salva pubblico**, segui questi passaggi:

1. Aggiungi un&#39;attività **Save audience** alla campagna orchestrata.

1. Nel menu a discesa **Modalità**, selezionare l&#39;azione che si desidera eseguire:

   * **Crea o aggiorna un pubblico esistente**: definisci una **etichetta pubblico**. Se il pubblico esiste già, viene aggiornato; in caso contrario, viene creato un nuovo pubblico.

   * **Aggiorna un pubblico esistente**: scegli il **pubblico** da aggiornare dall&#39;elenco dei tipi di pubblico esistenti.

1. Seleziona la **modalità di aggiornamento** applicabile ai tipi di pubblico esistenti:

   * **Sostituisci il contenuto del pubblico con nuovi dati**: tutto il contenuto del pubblico viene sostituito e i vecchi dati andranno persi. Vengono conservati solo i dati della transizione in entrata dell&#39;attività **Save audience**. Questa opzione elimina il tipo di pubblico e la dimensione di targeting del pubblico aggiornato.

   * **Pubblico completo con nuovi dati**: il contenuto del pubblico precedente viene mantenuto e i dati della transizione in entrata dell&#39;attività **Salva pubblico** vengono aggiunti a esso.

1. Seleziona l&#39;opzione **Genera una transizione in uscita** se desideri aggiungere una transizione dopo l&#39;attività **Salva pubblico**.

Il contenuto del pubblico salvato è quindi disponibile nella relativa visualizzazione dettagliata, accessibile dal menu **Tipi di pubblico**. Le colonne disponibili in questa visualizzazione corrispondono alle colonne della transizione in entrata dell&#39;attività **Save audience** della campagna orchestrata.

## Esempio {#save-audience-example}

L’esempio seguente illustra un semplice aggiornamento del pubblico dal targeting. Una pianificazione esegue la campagna orchestrata una volta al mese. Una query recupera tutti i profili abbonati alle diverse applicazioni disponibili. L&#39;attività **Save audience** aggiorna il pubblico rimuovendo i profili che hanno annullato l&#39;abbonamento al servizio dall&#39;ultima esecuzione della campagna orchestrata e aggiungendo i profili appena abbonati.
