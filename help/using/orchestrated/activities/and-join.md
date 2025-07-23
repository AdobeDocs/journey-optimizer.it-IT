---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività AND-join
description: Scopri come utilizzare l’attività AND-join in una campagna orchestrata
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 88%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Attività AND-join"
>abstract="L’attività **And-join** consente di sincronizzare più rami di esecuzione di una campagna orchestrata. Viene attivata al termine di tutte le attività precedenti. Questo consente di assicurarti che determinate attività siano state completate prima di continuare a eseguire la campagna orchestrata."


+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](../gs-schemas.md)</li><li>[Schema manuale](../manual-schema.md)</li><li>[Schema di caricamento file](../file-upload-schema.md)</li><li>[Acquisire dati](../ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Introduzione alle attività](about-activities.md)<br/><br/>Attività:<br/><b>[AND-join](and-join.md)</b> - [Crea pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplica](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

L’attività **[!UICONTROL AND-join]** è un’attività di **[!UICONTROL Controllo del flusso]**. Consente di sincronizzare più rami di esecuzione di una campagna orchestrata.

Questa attività attiva la relativa transizione in uscita solo dopo che tutte le transizioni in entrata sono state attivate; in altre parole, dopo che tutte le attività precedenti sono state completate. Questo consente di assicurarti che determinate attività siano state completate prima di continuare a eseguire la campagna orchestrata.

## Configurare l’attività And-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Opzioni di unione"
>abstract="Seleziona le attività che vuoi unire. Nel menu a discesa **Set primario**, scegli la popolazione di transizione in entrata da mantenere."

Per configurare l’attività **[!UICONTROL AND-join]**, segui questi passaggi:

![](../assets/workflow-andjoin.png)

1. Aggiungi più attività, come le attività del canale, per creare almeno due rami di esecuzione diversi.

1. Inserisci un’attività **[!UICONTROL AND-join]** in uno qualsiasi dei rami.

1. Nella sezione **[!UICONTROL Opzioni di unione]**, seleziona tutte le attività precedenti che desideri unire.

1. Nel menu a discesa **[!UICONTROL Set primario]**, scegli la popolazione di transizione in entrata da mantenere.

## Esempio{#and-join-example}

Questo esempio illustra due rami coordinati della campagna, ciascuno con una consegna e-mail, uno indirizzato ai membri di livello Gold e l’altro ai membri di livello Silver. **[!UICONTROL AND-join]** si attiva quando vengono attivate entrambe le transizioni in ingresso e l’SMS verrà inviato solo dopo il completamento di entrambe le consegne e-mail, dopo un ritardo di 7 giorni.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
