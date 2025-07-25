---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Combina
description: Scopri come utilizzare l’attività Combina
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: 1a9ea09fcbf304b1649a5ae88da34bd209e9ac8b
workflow-type: tm+mt
source-wordcount: '1135'
ht-degree: 96%

---

# Combina {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="Attività Combina"
>abstract="L’attività **Combina** consente di eseguire la segmentazione sulla popolazione in entrata. Puoi quindi combinare più popolazioni, escluderne una parte o mantenere i dati comuni a più target."

+++ Sommario

| Ti diamo il benvenuto nelle campagne orchestrate | Avviare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>Creazione e gestione di schemi e set di dati relazionali:</br> <ul><li>[Introduzione a schemi e set di dati](../gs-schemas.md)</li><li>[Schema manuale](../manual-schema.md)</li><li>[Schema di caricamento file](../file-upload-schema.md)</li><li>[Acquisire dati](../ingest-data.md)</li></ul>[Accedere e gestire le campagne orchestrate](../access-manage-orchestrated-campaigns.md) | [Passaggi chiave per creare una campagna orchestrata](../gs-campaign-creation.md)<br/><br/>[Creare e pianificare la campagna](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utilizzare il generatore di regole](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md)<br/><br/>[Retargeting](../retarget.md) | [Introduzione alle attività](about-activities.md)<br/><br/>Attività:<br/>[AND-join](and-join.md) - [Crea pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Attività canale](channels.md) - <b>[Combina](combine.md)</b> - [Deduplica](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Salva pubblico](save-audience.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Il contenuto di questa pagina non è definitivo e potrebbe essere soggetto a modifiche.

>[!ENDSHADEBOX]

L’attività **[!UICONTROL Combina]** è un tipo di attività di **[!UICONTROL targeting]** che permette di segmentare in modo efficace la popolazione in entrata. Consente di unire più popolazioni, escludere segmenti specifici o mantenere solo i dati condivisi tra più target.

Sono disponibili le seguenti opzioni di segmentazione:

* **[!UICONTROL Unione]**: raggruppa i risultati di più attività in un’unico target unificato.

* **[!UICONTROL Intersezione]**: conserva solo gli elementi comuni a tutte le popolazioni in entrata.

* **[!UICONTROL Esclusione]**: rimuove elementi da una popolazione in base a criteri specificati.

## Configurare l’attività Combina {#combine-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_merging_options"
>title="Opzioni di unione per Intersezione"
>abstract="L’attività Intersezione ti consente di mantenere solo gli elementi comuni alle diverse popolazioni in entrata all’interno dell’attività. Nella sezione Set da unire, seleziona tutte le attività precedenti che desideri unire."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_merging_options"
>title="Opzioni di unione per Esclusione"
>abstract="L’attività Esclusione consente di escludere elementi da una popolazione in base a determinati criteri. Nella sezione Set da unire, seleziona tutte le attività precedenti che desideri unire."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_options"
>title="Selezionare il tipo di segmentazione"
>abstract="Seleziona come combinare i tipi di pubblico. L’attività **Unione** consente di raggruppare il risultato di più attività in un’unica destinazione. L’attività **Intersezione** consente di mantenere solo gli elementi comuni alle diverse popolazioni in entrata nell’attività. L’attività **Esclusione** consente di escludere elementi da una popolazione in base a determinati criteri. "

Per iniziare a configurare l’attività **[!UICONTROL Combina]**, segui questi passaggi comuni:

![](../assets/orchestrated-union.png)

1. Aggiungi più attività, come le attività **[!UICONTROL Crea pubblico]**, per formare almeno due rami di esecuzione diversi.
1. Aggiungi un’attività **[!UICONTROL Combina]** ad uno dei rami precedenti.
1. Seleziona il tipo di segmentazione: [Unione](#union), [Intersezione](#intersection) o [Esclusione](#exclusion).
1. Fai clic su **[!UICONTROL Continua]**.
1. Nella sezione **[!UICONTROL Set da unire]**, seleziona tutte le attività precedenti che desideri unire.

## Unione {#combine-union}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_reconciliation"
>title="Opzioni di riconciliazione"
>abstract="Seleziona il **Tipo di riconciliazione** per definire la modalità di gestione dei duplicati. Per impostazione predefinita, l’opzione **Chiavi** è attivata, il che significa che l’attività mantiene un solo elemento quando gli elementi delle diverse transizioni in entrata hanno la stessa chiave. Utilizza l’opzione **Una seleziona di colonne** per definire l’elenco di colonne alle quali viene applicata la riconciliazione dei dati."

All’interno dell’attività **[!UICONTROL Combina]**, è possibile configurare un’**[!UICONTROL unione]** selezionando un **[!UICONTROL tipo di riconciliazione]** per determinare la modalità di gestione dei record duplicati:

* **[!UICONTROL Solo chiavi]** (impostazione predefinita): mantiene un singolo record quando più transizioni in entrata condividono la stessa chiave. È possibile utilizzare questa opzione solo se le popolazioni in entrata sono omogenee.

* **[!UICONTROL Una selezione di colonne]**: consente di specificare quali colonne vengono utilizzate per la riconciliazione dei dati. Seleziona **[!UICONTROL Aggiungi attributo]**.

Nell’esempio seguente viene utilizzata un’attività **[!UICONTROL Combina]** con un’**[!UICONTROL unione]** per unire i risultati di due query, **Membri fedeltà** e **Acquirenti**, in un unico pubblico più grande che include tutti i profili di entrambi i segmenti.

![](../assets/orchestrated-union-example.png)

## Intersezione {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="Opzioni di riconciliazione dell’intersezione"
>abstract="Seleziona il **Tipo di riconciliazione** per definire la modalità di gestione dei duplicati. Per impostazione predefinita, l’opzione **Chiavi** è attivata, il che significa che l’attività mantiene un solo elemento quando gli elementi delle diverse transizioni in entrata hanno la stessa chiave. Utilizza l’opzione **Una seleziona di colonne** per definire l’elenco di colonne alle quali viene applicata la riconciliazione dei dati."

Nell’attività **[!UICONTROL Combina]**, puoi configurare un’**[!UICONTROL Intersezione]**. A questo scopo, segui i passaggi aggiuntivi riportati di seguito:

1. Seleziona il **[!UICONTROL Tipo di riconciliazione]** per definire la modalità di gestione dei duplicati.

   * **[!UICONTROL Solo chiavi]** (impostazione predefinita): mantiene un singolo record quando più transizioni in entrata condividono la stessa chiave. È possibile utilizzare questa opzione solo se le popolazioni in entrata sono omogenee.

   * **[!UICONTROL Una selezione di colonne]**: consente di specificare quali colonne vengono utilizzate per la riconciliazione dei dati. Seleziona **[!UICONTROL Aggiungi attributo]**.

1. Se desideri sfruttare la popolazione rimanente, abilita l’opzione **[!UICONTROL Genera complemento]**. Il complemento contiene l’unione di tutti i risultati dell’attività in entrata, esclusa l’intersezione. All’attività verrà quindi aggiunta un’ulteriore transizione in uscita.

L’esempio seguente mostra l’uso dell’**[!UICONTROL intersezione]** tra due attività di query. Viene utilizzata per identificare i profili che sono **membri fedeltà** e che hanno effettuato un acquisto nell’ultimo mese.

![](../assets/orchestrated-intersection-example.png)


## Esclusione {#combine-exclusion}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_exclusion_options"
>title="Regole di esclusione"
>abstract="Se necessario, è possibile elaborare le tabelle in entrata. In effetti, per escludere un target da un’altra dimensione, tale target deve essere restituito nella stessa dimensione targeting del target principale. A questo scopo, nella sezione Regole di esclusione, fai clic su Aggiungi una regola e specifica le condizioni di modifica della dimensione. La riconciliazione dei dati viene eseguita tramite un attributo o un’unione."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_sets"
>title="Selezionare i set da combinare"
>abstract="Nella sezione **Set da unire**, dalle transizioni in entrata, seleziona **Set primario**. Questo è il set da cui gli elementi sono esclusi. Gli altri set confrontano gli elementi prima che vengano esclusi dal set primario."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_exclusion"
>title="Regole di esclusione"
>abstract="Se necessario, è possibile elaborare le tabelle in entrata. In effetti, per escludere un target da un’altra dimensione, tale target deve essere restituito nella stessa dimensione targeting del target principale. A questo scopo, nella sezione Regole di esclusione, fai clic su Aggiungi una regola e specifica le condizioni di modifica della dimensione. La riconciliazione dei dati viene eseguita tramite un attributo o un’unione."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine_complement"
>title="Complemento generato da combinazione"
>abstract="Attiva l’opzione Genera complemento per elaborare la popolazione rimanente in una transizione aggiuntiva."

Nell’attività **[!UICONTROL Combina]**, puoi configurare un’**[!UICONTROL Esclusione]**. A questo scopo, segui i passaggi aggiuntivi riportati di seguito:

1. Nella sezione **[!UICONTROL Set da unire]**, scegli il **[!UICONTROL Set primario]** che rappresenta la popolazione principale. I record trovati negli altri set sono esclusi da questo set primario.

1. Se necessario, puoi regolare le tabelle in entrata per allineare i target da dimensioni diverse. Per escludere un target da un’altra dimensione, tale target deve essere portato nella stessa dimensione targeting della popolazione principale. A tale scopo, fai clic su **[!UICONTROL Aggiungi una regola]** e definisci le condizioni per la modifica della dimensione. La riconciliazione viene quindi eseguita utilizzando un attributo o un’unione.

1. Se desideri elaborare la popolazione rimanente, abilita l’opzione **[!UICONTROL Genera complemento]**. Il complemento contiene l’unione di tutti i risultati dell’attività in entrata, esclusa l’intersezione. All’attività verrà quindi aggiunta un’ulteriore transizione in uscita.

L’esempio seguente di **[!UICONTROL esclusione]** mostra due query configurate per filtrare i profili che hanno acquistato un prodotto. I profili che non dispongono di una tessera fedeltà vengono quindi esclusi dal primo set.

![](../assets/orchestrated-exclusion-example.png)

