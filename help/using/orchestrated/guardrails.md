---
solution: Journey Optimizer
product: journey optimizer
title: Guardrail e limitazioni delle campagne orchestrate
description: Scopri le limitazioni e i guardrail delle campagne orchestrate
hide: true
hidefromtoc: true
source-git-commit: 54d5b3386da4eed53fca79a2135ab54548855150
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 11%

---

# Guardrail e limitazioni {#guardrails}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Pubblicare una campagna orchestrata"
>abstract="Per avviare la campagna, è necessario pubblicarla. Assicurati che tutti gli avvisi siano cancellati prima della pubblicazione."

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](configuration-steps.md)<br/><br/>[Accesso e gestione delle campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Crea e pianifica la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrazione attività](orchestrate-activities.md)<br/><br/>[Avvia e monitora la campagna](start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Inizia a usare le attività](activities/about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](activities/and-join.md) - [Genera pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplicazione](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

## Limitazioni del flusso di dati rispetto al set di dati

Ogni set di dati in Adobe Experience Platform può essere associato a un solo flusso di dati attivo alla volta. Questa cardinalità 1:1 è rigorosamente applicata dalla piattaforma.

Se devi cambiare origine dati (ad esempio, da Amazon S3 a Salesforce):

Devi eliminare il flusso di dati esistente connesso al set di dati.

Quindi, crea un nuovo flusso di dati con la nuova origine mappata sullo stesso set di dati.

Questo garantisce l’acquisizione affidabile dei dati ed è essenziale quando si utilizza Change Data Capture (CDC), che dipende da una chiave primaria definita e da un attributo di controllo delle versioni (ad esempio, lastmodified) per gli aggiornamenti incrementali.


## Schemi relazionali/limitazioni dell’acquisizione dei dati

* Numero di schemi: il numero massimo di schemi relazionali (tabelle nell’archivio dati relazionale) è 200
* Dimensione schema relazionale: la dimensione massima dello schema relazionale per l’orchestrazione delle campagne è di 100 GB.
* Frequenza di acquisizione dei dati: la frequenza di acquisizione dei dati in batch per l’orchestrazione delle campagne non deve superare una ogni quindici minuti.
* Modifiche/aggiornamenti: gli aggiornamenti/modifiche giornalieri devono essere inferiori al 20% dei record totali per un determinato schema relazionale