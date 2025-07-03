---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Attendi nelle campagne orchestrate
description: Scopri come utilizzare l’attività Attendi nelle campagne orchestrate
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 8a5026cdeb63b7b261ec0dfa690c5bd41d7de772
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 13%

---

# Attendi {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Attività Attendi"
>abstract="L’attività **Attendi** viene utilizzata per ritardare la transizione da un’attività a un’altra."


+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](../configuration-steps.md)<br/><br/>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per la creazione orchestrata della campagna](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa e unisci](and-join.md) - [Genera pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](split.md) - <b>[Attendi](wait.md)</b> |

{style="table-layout:fixed"}

+++


<br/>

L&#39;attività **[!UICONTROL Wait]** è un componente del **[!UICONTROL controllo di flusso]** utilizzato per introdurre un ritardo tra due attività in una campagna orchestrata. In questo modo le attività di follow-up saranno più tempestive e rilevanti per il coinvolgimento degli utenti.

Ad esempio, puoi attendere alcuni giorni dopo una consegna e-mail per tenere traccia di aperture e clic prima di inviare un messaggio di follow-up.

## Configurazione{#wait-configuration}

Per configurare l’attività **[!UICONTROL Attendi]**, segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Wait]** alla campagna orchestrata.

1. Selezionare il tipo di attesa più adatto alle proprie esigenze:

   * **[!UICONTROL Durata]**: specifica un ritardo in secondi, minuti, ore o giorni prima di procedere all&#39;attività successiva.

   * **[!UICONTROL Ora fissa]**: imposta una data e un&#39;ora specifiche dopo le quali inizia l&#39;attività successiva.

   ![](../assets/wait_activity.png)

## Esempio{#wait-example}

L&#39;esempio seguente illustra l&#39;attività **[!UICONTROL Wait]** in un caso d&#39;uso tipico.  Un’e-mail con un codice promozionale viene inviata ai profili che festeggiano il loro compleanno. Dopo 29 giorni, un SMS viene inviato allo stesso gruppo come promemoria che il loro codice promozionale di compleanno sta per scadere.

![](../assets/wait-example.png)
