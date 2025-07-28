---
solution: Journey Optimizer
product: journey optimizer
title: Passaggi chiave per creare una campagna orchestrata
description: Scopri i principi chiave della creazione di campagne orchestrate con Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Passaggi chiave per creare una campagna orchestrata {#orchestrated-campaign-creation}

+++ Sommario

| Benvenuto in Campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/><b>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md)</b> | [Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Introduzione alle attività](activities/about-activities.md)<br/><br/>Attività:<br/>[AND-join](activities/and-join.md) - [Crea pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplica](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

Questa pagina illustra i passaggi essenziali per creare e avviare una campagna orchestrata, dalla configurazione e progettazione al monitoraggio e reporting.

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="#create"><img alt="Create & schedule your campaign" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="#create"><strong>Create & schedule your campaign</strong></a></td>
<td><a href="#orchestrate"><img alt="Orchestrate campaign activities" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="#orchestrate"><strong>Orchestrate campaign activities</strong></a></td>
<td><a href="#start"><img alt="Start & monitor your campaign" src="../../channels/assets/do-not-localize/push.png"></a><a href="#start"><strong>Start & monitor your campaign</strong></a></td>
<td><a href="#report"><img alt="Analyze & report on results" src="../../channels/assets/do-not-localize/push.png"></a><a href="#report"><strong>Analyze & report on results</strong></a></td>
</tr></table>-->



## Passaggio 1: creare e pianificare la campagna {#create}

Prima di tutto, devi creare la tua campagna orchestrata e definire *quando* deve essere eseguita. Che si tratti di una campagna push una tantum o di una campagna multicanale ricorrente, avrai il pieno controllo su tempistica e frequenza.

➡️ [Scopri come creare e pianificare una campagna](../orchestrated/create-orchestrated-campaign.md).

## Passaggio 2: orchestrare le attività della campagna {#orchestrate}

Una volta creata la campagna, è il momento di progettare la logica che sta alla base. Utilizzando un’area di lavoro visiva, puoi combinare attività di targeting, consegna e controllo del flusso per modellare l’esperienza cliente.

➡️ [Scopri come orchestrare le attività](../orchestrated/orchestrate-activities.md)

## Passaggio 3: avviare e monitorare la campagna {#start}

Ci sei quasi! Esegui prima la campagna in modalità di test per individuare eventuali problemi. Quindi pubblicala e monitora l’esecuzione live in tempo reale: tieni traccia dell’avanzamento, verifica la presenza di errori e osserva come fluiscono i profili in ogni passaggio.

➡️ [Scopri come avviare e monitorare una campagna](../orchestrated/start-monitor-campaigns.md).

## Passaggio 4: analisi e rapporto sui risultati {#report}

Dopo l’avvio, utilizza i rapporti incorporati per capire cosa ha funzionato e cosa potrebbe essere migliorato. Le dashboard in tempo reale e le analisi approfondite consentono di ottimizzare le campagne future e di perfezionare la strategia.

➡️ [Ulteriori informazioni sul reporting](../orchestrated/reporting-campaigns.md)

## Per andare oltre: eseguire il retargeting in base al coinvolgimento {#retarget}

Una volta eseguita la campagna, puoi fare un ulteriore passo avanti eseguendo il retargeting dei profili in base al modo in cui hanno interagito con il messaggio, sia che lo abbiano aperto o fatto clic su un collegamento. Questo consente di rispondere con messaggi personalizzati, coinvolgere nuovamente gli utenti inattivi o raddoppiare l’interesse.

➡️ [Scopri come eseguire il retargeting in base agli eventi di feedback](../orchestrated/retarget.md)
