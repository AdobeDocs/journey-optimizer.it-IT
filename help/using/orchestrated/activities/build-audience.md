---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Crea pubblico
description: Scopri come utilizzare l’attività Crea pubblico in una campagna orchestrata
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 89%

---

# Crea pubblico {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Attività Crea pubblico"
>abstract="L’attività **Crea pubblico** ti consente di definire il pubblico che entrerà nella campagna orchestrata. Quando si inviano messaggi nel contesto di una campagna orchestrata, il pubblico del messaggio non è definito nell’attività del canale, ma nell’attività **Crea pubblico**."

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](../gs-schemas.md)</li><li>[Schema manuale](../manual-schema.md)</li><li>[Schema di caricamento file](../file-upload-schema.md)</li><li>[Acquisire dati](../ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Introduzione alle attività](about-activities.md)<br/><br/>Attività:<br/>[AND-join](and-join.md) - <b>[Crea pubblico](build-audience.md)</b> - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplica](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++


<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

In qualità di marketer, puoi creare segmenti di pubblico complessi tramite un’interfaccia intuitiva, che ti consente di eseguire il targeting degli utenti in base a un’ampia gamma di criteri e comportamenti per adattare le campagne in modo più efficace.

A questo scopo, utilizza l’attività di targeting **[!UICONTROL Crea pubblico]**. Questa attività definisce il pubblico che entra nella campagna orchestrata. Durante l’invio di messaggi come parte di una campagna orchestrata, il pubblico viene definito nell’attività **[!UICONTROL Crea pubblico]**, non all’interno della campagna orchestrata.

## Configurare l’attività Crea pubblico {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Pubblico"
>abstract="Seleziona il pubblico nello stesso modo in cui utilizzi un pubblico durante la progettazione di una nuova consegna."

Per configurare l’attività **[!UICONTROL Crea pubblico]**, segui questi passaggi:

1. Aggiungi un’attività **[!UICONTROL Crea pubblico]**.

   ![](../assets/build-audience.png)

1. Definisci un’**[!UICONTROL etichetta]**.

1. Configura il pubblico seguendo i passaggi descritti nelle schede seguenti.

1. Scegli la **[!UICONTROL Dimensione targeting]**. La dimensione targeting consente di definire la popolazione target dell’operazione: destinatari, beneficiari del contratto, operatore, iscritti, ecc. Per impostazione predefinita, il target viene selezionato dai destinatari.

1. Fai clic su **[!UICONTROL Continua]**.

1. Utilizza il query modeler per definire la query. [Ulteriori informazioni sul query modeler sono disponibili in questa sezione](../orchestrated-rule-builder.md).

1. Specifica se deve essere generata una transizione in uscita quando il pubblico è vuoto.

## Esempi{#build-audience-examples}

Di seguito è riportato un esempio di una campagna orchestrata con due attività **[!UICONTROL Crea pubblico]**. La prima esegue il targeting dei profili che hanno elementi nel carrello, seguito da una consegna e-mail. La seconda esegue il targeting dei profili con una wishlist, seguito da una consegna SMS.

![](../assets/build-audience-2.png)
