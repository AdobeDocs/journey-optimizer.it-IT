---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività AND-join
description: Scopri come utilizzare l’attività AND-join in una campagna orchestrata
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 1b99313e-f131-44f7-a129-f85e1977fb05
source-git-commit: 7de878c316e966129e7dede37f132938d2abbdf8
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 38%

---

# AND-join {#join}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join"
>title="Attività AND-join"
>abstract="L’attività **And-join** consente di sincronizzare più rami di esecuzione di una campagna orchestrata. Viene attivata al termine di tutte le attività precedenti. Questo consente di assicurarti che determinate attività siano state completate prima di continuare a eseguire la campagna orchestrata."

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](../configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](../gs-campaign-creation.md) | [Creare una campagna orchestrata](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](and-join.md) - [Genera pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

L’attività **[!UICONTROL Unione AND]** è un’attività di **[!UICONTROL Controllo del flusso]**. Consente di sincronizzare più rami di esecuzione di una campagna orchestrata.

Questa attività attiva la relativa transizione in uscita solo dopo che tutte le transizioni in entrata sono state attivate, in altre parole, dopo che tutte le attività precedenti sono state completate. Questo ti consente di verificare che alcune attività siano state completate prima di continuare a eseguire la campagna orchestrata.

## Configurare l’attività And-join{#and-join-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_and-join_merging"
>title="Opzioni di unione"
>abstract="Seleziona le attività che vuoi unire. Nel menu a discesa **Set primario**, scegli la popolazione di transizione in entrata da mantenere."

Per configurare l’attività **[!UICONTROL Unione AND]**, segui questi passaggi:

![](../assets/workflow-andjoin.png)

1. Aggiungi più attività, ad esempio attività canale, per creare almeno due rami di esecuzione distinti.

1. Inserire un&#39;attività **[!UICONTROL AND-join]** in uno dei rami.

1. Nella sezione **[!UICONTROL Opzioni di unione]**, seleziona tutte le attività precedenti a cui desideri partecipare.

1. Dall&#39;elenco a discesa **[!UICONTROL Set primario]**, scegliere il gruppo di transizione in entrata che si desidera mantenere.

## Esempio{#and-join-example}

Questo esempio illustra due rami coordinati della campagna, ciascuno con una consegna e-mail, uno indirizzato ai membri gold e l’altro silver. **[!UICONTROL AND-join]** si attiva quando vengono attivate entrambe le transizioni in ingresso e l&#39;SMS verrà inviato solo dopo il completamento di entrambe le consegne e-mail, dopo un ritardo di 7 giorni.

![](../assets/workflow-andjoin-example.png){zoomable="yes"}
