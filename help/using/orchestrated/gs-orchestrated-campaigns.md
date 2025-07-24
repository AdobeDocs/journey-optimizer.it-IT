---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle campagne orchestrate
description: Scopri come iniziare a utilizzare le campagne orchestrate
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 611dd06d-aa18-4fa3-a477-8a910cec21d8
source-git-commit: 4f881bfc32a5f168a93b51c9a69398881790050c
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 18%

---

# Introduzione alle campagne orchestrate {#orchestrated-camp}

>[!CONTEXTUALHELP]
>id="campaigns_overview_orchestrated"
>title="campaign_overview_orchestrated"
>abstract="<b>Orchestrazione campagna</b><br/>Dividi, combina, arricchisci e gestisci i set di dati relazionali per definire il pubblico<br/><br/>

<b>Sfruttare dati con più entità</b><br/>Scopri in che modo le campagne orchestrate possono sfruttare i set di dati relazionali per arricchire i dati per la segmentazione e la personalizzazione<br/><br/><b>Segmentazione ad hoc e conteggi esatti</b><br/>Crea il segmento passo dopo passo con conteggi esatti<br/><br/><b>Canali disponibili</b><br/>E-mail, SMS, notifiche push, direct mail&quot;

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| <b>[Introduzione alle campagne orchestrate](gs-orchestrated-campaigns.md)</b><br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](gs-schemas.md)</li><li>[Schema manuale](manual-schema.md)</li><li>[Schema di caricamento file](file-upload-schema.md)</li><li>[Acquisire dati](ingest-data.md)</li></ul>[Accedere e gestire campagne orchestrate](access-manage-orchestrated-campaigns.md)<br/><br/>[Passaggi chiave per creare una campagna orchestrata](gs-campaign-creation.md) | [Creare e pianificare la campagna](create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utilizzare il generatore di regole](orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](build-query.md)<br/><br/>[Modificare le espressioni](edit-expressions.md)<br/><br/>[Retargeting](retarget.md) | [Introduzione alle attività](activities/about-activities.md)<br/><br/>Attività:<br/>[AND-join](activities/and-join.md) - [Crea pubblico](activities/build-audience.md) - [Modifica dimensione](activities/change-dimension.md) - [Attività canale](activities/channels.md) - [Combina](activities/combine.md) - [Deduplica](activities/deduplication.md) - [Arricchimento](activities/enrichment.md) - [Fork](activities/fork.md) - [Riconciliazione](activities/reconciliation.md) - [Salva pubblico](activities/save-audience.md) - [Dividi](activities/split.md) - [Attendi](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

L&#39;orchestrazione delle campagne in [!DNL Adobe Journey Optimizer] potenzia campagne di marketing sofisticate e avviate dal brand su tutti i canali, aiutandoti a incrementare il coinvolgimento, i ricavi e la fedeltà dei clienti su larga scala.

Anche se il marketing cross-channel è essenziale, le campagne orchestrate lo rendono semplice. Grazie a un’interfaccia visiva basata su un trascinamento della selezione, puoi progettare e automatizzare flussi di lavoro di marketing complessi, dalla segmentazione alla distribuzione dei messaggi, su più canali. Tutto avviene in un ambiente intuitivo, progettato per velocità, controllo ed efficienza.

![](assets/canvas-example-diagram.png){zoomable="yes"}

## Funzionalità di base

L’orchestrazione delle campagne si basa su quattro pilastri chiave:

<table style="table-layout:auto">
<tr style="border: 0;">
<td><img alt="Pubblico on-demand" src="assets/do-not-localize/icon-audience.svg" width="50px"></a></td><td><b>Tipi di pubblico su richiesta</b><br/>Esegui una query istantanea tra set di dati per creare segmenti di pubblico utilizzando qualsiasi combinazione di tipi di dati e dimensioni.</td></tr>
<tr style="border: 0;">
<td><img alt="Segmentazione e invio di più entità" src="assets/do-not-localize/icon-entity.svg" width="50px"></a></td><td><b>Segmentazione e invio di più entità</b><br/>Oltre alle campagne basate su persone, utilizza entità quali cataloghi di prodotti, posizioni di store o dati del servizio per eseguire il targeting con precisione.</td></tr>
<tr style="border: 0;">
<td><img alt="Visibilità e precisione pre-invio" src="assets/do-not-localize/icon-visibility.svg" width="50px"></a></td><td><b>Visibilità e precisione pre-invio</b><br/>Ottieni conteggi di segmentazione esatti e ambito completo della campagna prima del lancio, garantendo precisione e affidabilità.</td></tr>
<tr style="border: 0;">
<td><img alt="Flussi di lavoro per campagne in più passaggi" src="assets/do-not-localize/icon-multistep.svg" width="50px"></a></td><td><b>Flussi di lavoro per campagne con più passaggi</b><br/>Progetta campagne con più passaggi, dai messaggi giornalieri alle campagne complesse come le promozioni stagionali o i principali lanci di prodotti.</td></tr>
</table>

## Campagne e percorsi orchestrati

Anche se la visualizzazione delle campagne orchestrate ha somiglianze con i percorsi, risolve diversi scopi e casi d’uso:

* **Percorsi** - da 1 a 1 area di lavoro in cui ogni profilo viaggia attraverso i diversi passaggi al proprio ritmo. Lo stato di ciascun cliente viene mantenuto nel suo contesto per attivare azioni in tempo reale.

* **Campagne orchestrate** - A differenza dei percorsi, le campagne orchestrate funzionano utilizzando un&#39;area di lavoro batch che calcola i segmenti. Tutti i profili vengono elaborati contemporaneamente.

## Prerequisiti

Prima di lavorare con le campagne orchestrate, è essenziale assicurarsi di disporre delle autorizzazioni appropriate. L&#39;accesso alle campagne orchestrate è limitato agli utenti assegnati a un **[!UICONTROL profilo di prodotto]** rilevante, ad esempio Amministratore campagna orchestrata, Approvatore campagna orchestrata, Gestore campagna orchestrata o Visualizzatore campagna orchestrata.

Se non riesci ad accedere alle funzionalità della campagna orchestrata, contatta l’amministratore per richiedere le autorizzazioni necessarie.

➡️ [Ulteriori informazioni sui profili di prodotto relativi alle campagne orchestrate](../administration/ootb-product-profiles.md)

## Approfondiamo

Ora che hai capito cosa sono le campagne organizzate, è ora di approfondire queste sezioni della documentazione per iniziare a lavorare con questa funzione.

<table><tr style="border: 0; text-align: center;">
<td>
<a href="gs-campaign-creation.md">
<img alt="Accedere e gestire i flussi di lavoro" src="assets/do-not-localize/workflow-access.jpeg">
</a>
<div>
<a href="gs-campaign-creation.md"><strong>Passaggi di configurazione</strong></a>
</div>
<p>
</td>
<td>
<a href="create-orchestrated-campaign.md">
<img alt="Lead" src="assets/do-not-localize/workflow-create.jpeg">
</a>
<div><a href="create-orchestrated-campaign.md"><strong>Creare una campagna orchestrata</strong>
</div>
<p>
</td>
<td>
<a href="activities/about-activities.md">
<img alt="Non frequente" src="assets/do-not-localize/workflow-activities.jpeg">
</a>
<div>
<a href="activities/about-activities.md"><strong>Utilizzare le attività</strong></a>
</div>
<p></td>
</tr></table>
