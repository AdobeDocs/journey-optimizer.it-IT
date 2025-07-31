---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Test nelle campagne orchestrate
description: Scopri come utilizzare l’attività Test
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: edd70849-0a21-45f2-91f3-4774a0cad9dd
source-git-commit: 458e0b19725147e0a3ad34891ca55b61f1ac44a8
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 59%

---

# Test {#test}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test"
>title="Attività di test"
>abstract="L’attività **Test** è un’attività di **Controllo del flusso**. Consente di abilitare le transizioni in base a condizioni specificate."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_test_conditions"
>title="Condizioni"
>abstract="L&#39;attività **Test** può avere più transizioni di output. Durante l’esecuzione della campagna orchestrata, ogni condizione viene testata in sequenza fino a quando non ne viene soddisfatta una. Se nessuna delle condizioni è soddisfatta, la campagna orchestrata continua lungo il percorso della **[!UICONTROL condizione predefinita]**. Se non viene attivata alcuna condizione predefinita, la campagna orchestrata si interrompe a questo punto."

+++ Sommario

| Benvenuto in Campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](../gs-schemas.md)</li><li>[Schema manuale](../manual-schema.md)</li><li>[Schema di caricamento file](../file-upload-schema.md)</li><li>[Acquisire dati](../ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Introduzione alle attività](about-activities.md)<br/><br/>Attività:<br/>[AND-join](and-join.md) - [Crea pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplica](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

L’attività **[!UICONTROL Test]** è un’attività di **[!UICONTROL Controllo del flusso]**. Consente di abilitare le transizioni in base a condizioni specificate.

## Configurare l’attività Test {#test-configuration}

Per configurare l’attività **[!UICONTROL Test]** segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Test]** alla campagna orchestrata.

1. Per impostazione predefinita, l’attività **[!UICONTROL Test]** presenta un semplice test booleano. Se la condizione definita nella transizione “True” è soddisfatta, questa transizione verrà attivata. In caso contrario, verrà attivata una transizione predefinita “False”.

1. Per configurare la condizione associata a una transizione, fai clic sull’icona **[!UICONTROL Apri finestra di personalizzazione]**. Utilizza l’editor di espressioni per definire le regole necessarie per attivare questa transizione. Puoi anche sfruttare le variabili evento, le condizioni e le funzioni data/ora.

   Inoltre, puoi modificare il campo **[!UICONTROL Etichetta]** per personalizzare il nome della transizione nell&#39;area di lavoro della campagna orchestrata.

   ![](../assets/workflow-test-default.png)

1. Puoi aggiungere più transizioni di output a un’attività **[!UICONTROL Test]**. A tale scopo, fai clic sul pulsante **[!UICONTROL Aggiungi condizione]** e configura l’etichetta e la condizione associata per ogni transizione.
v
1. Durante l’esecuzione della campagna orchestrata, ogni condizione viene testata in sequenza fino a quando non ne viene soddisfatta una. Se nessuna delle condizioni è soddisfatta, le campagne orchestrate continuano lungo il percorso della **[!UICONTROL condizione predefinita]**. Se non viene attivata alcuna condizione predefinita, la campagna si interrompe a questo punto.

## Esempio {#example}

In questo esempio vengono attivate diverse transizioni in base al numero di profili interessati da un’attività **[!UICONTROL Crea pubblico]**:

* Se il targeting riguarda più di 10.000 profili, viene inviato un messaggio e-mail.
* Per un numero di profili compreso tra 1.000 e 10.000, viene inviato un SMS.
* Se i profili target scendono al di sotto di 1.000, vengono indirizzati a una transizione “non contattare”.

![](../assets/workflow-test-example.png)

A questo scopo, la variabile dell’evento `vars.recCount` è stata utilizzata nelle condizioni “e-mail” e “sms” per contare il numero di profili target e attivare la transizione appropriata.

![](../assets/workflow-test-example-config.png)
