---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività di riconciliazione
description: Scopri come utilizzare l’attività Reconciliation in una campagna orchestrata
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 0d5cfffe-bc6c-40bc-b3e1-5b44368ac76f
source-git-commit: 458e0b19725147e0a3ad34891ca55b61f1ac44a8
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 75%

---

# Riconciliazione {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Attività di riconciliazione"
>abstract="L’attività di **riconciliazione** è un’attività di **targeting** che consente di definire il collegamento tra Adobe Journey Optimizer e i dati in una tabella di lavoro."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Campo di selezione riconciliazione"
>abstract="Campo di selezione riconciliazione"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Condizione di creazione riconciliazione"
>abstract="Condizione di creazione riconciliazione"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Complemento generato da riconciliazione"
>abstract="Complemento generato da riconciliazione"


+++ Sommario

| Benvenuto in Campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](../gs-schemas.md)</li><li>[Schema manuale](../manual-schema.md)</li><li>[Schema di caricamento file](../file-upload-schema.md)</li><li>[Acquisire dati](../ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Introduzione alle attività](about-activities.md)<br/><br/>Attività:<br/>[AND-join](and-join.md) - [Crea pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - [Combina](combine.md) - [Deduplica](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - <b>[Riconciliazione](reconciliation.md)</b> - [Salva pubblico](save-audience.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

L’attività di **[!UICONTROL riconciliazione]** è un’attività di **[!UICONTROL targeting]** che consente di definire il collegamento tra i dati nel database di Adobe Journey Optimizer e i dati in una tabella di lavoro, ad esempio i dati caricati da un file esterno.

L&#39;attività **[!UICONTROL Enrichment]** ti consente di aggiungere dati aggiuntivi alla campagna orchestrata, ad esempio combinando dati provenienti da più origini o collegandoli a una risorsa temporanea. L’attività **[!UICONTROL riconciliazione]** viene invece utilizzata per combinare dati non identificati o esterni con risorse esistenti nel database.

La **[!UICONTROL riconciliazione]** richiede che i record correlati esistano già nel sistema. Ad esempio, se importi un file di acquisto con l’elenco di prodotti, marche temporali e informazioni sulla clientela, sia i prodotti che la clientela stessa devono già essere presenti nel database per stabilire il collegamento.

## Configurare l’attività di riconciliazione {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Dimensione targeting"
>abstract="Seleziona la nuova dimensione targeting. Una dimensione consente di definire la popolazione target: destinatari, abbonati all’app, operatori, iscritti, ecc. Per impostazione predefinita, è selezionata la dimensione targeting corrente."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Regole di riconciliazione"
>abstract="Seleziona le regole di riconciliazione da utilizzare per la deduplica. Per utilizzare gli attributi, seleziona l’opzione **Attributi semplici** e scegli i campi di origine e di destinazione. Per creare una condizione di riconciliazione personalizzata utilizzando il generatore di regole, selezionare l&#39;opzione **Condizioni di riconciliazione avanzate**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Selezionare una dimensione targeting"
>abstract="Seleziona la dimensione targeting per i dati in entrata per cui eseguire la riconciliazione."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=it#targeting-dimensions" text="Dimensioni targeting"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Mantenere i dati non riconciliati"
>abstract="Per impostazione predefinita, i dati non riconciliati vengono conservati nella transizione in uscita e sono disponibili nella tabella di lavoro per utilizzi futuri. Per rimuovere i dati non riconciliati, disattiva l’opzione **Mantieni i dati non riconciliati**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Attributo di riconciliazione"
>abstract="Seleziona l’attributo da utilizzare per riconciliare i dati e fai clic su Conferma."

Per configurare l’attività **[!UICONTROL riconciliazione]** segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Reconciliation]** all&#39;area di lavoro.

1. Scegli una nuova dimensione targeting per definire su chi stai eseguendo il targeting, ad esempio destinatari o abbonati.

1. Imposta i campi da utilizzare per la corrispondenza dei dati in arrivo con i profili esistenti.

1. Per associare i dati utilizzando i campi di base, seleziona **[!UICONTROL Attributi semplici]**.

1. Imposta i campi corrispondenti:

   * **[!UICONTROL Origine]**: elenca i campi dati in arrivo.

   * **[!UICONTROL Destinazione]**: fa riferimento ai campi nella dimensione targeting selezionata.

   Una corrispondenza si verifica quando entrambi i valori sono uguali, ad esempio, corrispondenza per **[!UICONTROL e-mail]** per identificare i profili.

   ![](../assets/workflow-reconciliation-criteria.png)

1. Per aggiungere altre regole corrispondenti, fai clic su **[!UICONTROL Aggiungi regola]**. Affinché si verifichi una corrispondenza, è necessario che tutte le condizioni siano soddisfatte.

1. Per condizioni più complesse, scegli **[!UICONTROL Condizioni di riconciliazione avanzate]**. Utilizza il [generatore di regole](../orchestrated-rule-builder.md) per definire la logica personalizzata.

1. Per filtrare i dati da riconciliare, fare clic su **[!UICONTROL Crea filtro]** e definire la condizione nel generatore di regole.

1. Per impostazione predefinita, i record senza corrispondenza vengono conservati nella transizione in uscita e archiviati nella tabella di lavoro. Per rimuoverli, abilita l’opzione **[!UICONTROL Mantieni dati non riconciliati]**.

## Esempio {#example-reconciliation}

Questo esempio utilizza l’attività di **[!UICONTROL riconciliazione]** in Adobe Journey Optimizer per garantire che le e-mail vengano inviate solo alla clientela riconosciuta. I dati fluiscono attraverso un’attività **[!UICONTROL Leggi pubblico]** che esegue il targeting degli utenti con gli ordini precedenti. L’attività di **[!UICONTROL riconciliazione]** associa quindi questi dati in arrivo ai profili esistenti nel database utilizzando il campo e-mail.

![](../assets/workflow-reconciliation-sample-1.0.png)
