---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Combina
description: Scopri come utilizzare l’attività Combina
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: af3c3a9c-8172-43b0-bba1-4a3d068b9a9e
source-git-commit: cb335fd5610d70d801ae1c32dfe4d3ca9d1160ab
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 76%

---

# Combina {#combine}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_combine"
>title="Attività Combina"
>abstract="L’attività **Combina** consente di eseguire la segmentazione sulla popolazione in entrata. Puoi quindi combinare più popolazioni, escluderne una parte o mantenere i dati comuni a più target."

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](../configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](../gs-campaign-creation.md) | [Creare una campagna orchestrata](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Inviare messaggi con le campagne orchestrate](../send-messages.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](and-join.md) - [Genera pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

L&#39;attività **[!UICONTROL Combine]** è un tipo di attività **[!UICONTROL Targeting]** che consente di segmentare in modo efficace il gruppo in entrata. Consente di unire più popolazioni, escludere segmenti specifici o mantenere solo i dati condivisi tra più destinazioni.

Sono disponibili le seguenti opzioni di segmentazione:

* **[!UICONTROL Unione]**: unisce i risultati di più attività in un&#39;unica destinazione unificata.

* **[!UICONTROL Intersezione]**: conserva solo gli elementi comuni a tutte le popolazioni in entrata.

* **[!UICONTROL Esclusione]**: rimuove elementi da un gruppo in base a criteri specificati.

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

![](../assets/orchestrated-combine.png)

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

Nell’attività **[!UICONTROL Combina]**, puoi configurare un’**[!UICONTROL Unione]**. Per l’attività Unione, è necessario selezionare il **[!UICONTROL Tipo di riconciliazione]** per definire la modalità di gestione dei duplicati:

* **[!UICONTROL Solo chiavi]**: è la modalità predefinita. L’attività mantiene un solo elemento quando gli elementi delle diverse transizioni in entrata hanno la stessa chiave. È possibile utilizzare questa opzione solo se le popolazioni in entrata sono omogenee.
* **[!UICONTROL Una seleziona di colonne]**: seleziona questa opzione per definire l’elenco di colonne alle quali viene applicata la riconciliazione dei dati. Innanzitutto è necessario selezionare il set primario (quello contenente i dati di origine), quindi le colonne da utilizzare per l’unione.

Nell&#39;esempio seguente viene utilizzata un&#39;attività **[!UICONTROL Combine]** e viene aggiunta una **[!UICONTROL Union]** per recuperare tutti i profili delle due query: membri fedeltà e acquirenti per formare un pubblico più ampio.

![](../assets/orchestrated-union-example.png)

## Intersezione {#combine-intersection}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_intersection_reconciliation_options"
>title="Opzioni di riconciliazione dell’intersezione"
>abstract="Seleziona il **Tipo di riconciliazione** per definire la modalità di gestione dei duplicati. Per impostazione predefinita, l’opzione **Chiavi** è attivata, il che significa che l’attività mantiene un solo elemento quando gli elementi delle diverse transizioni in entrata hanno la stessa chiave. Utilizza l’opzione **Una seleziona di colonne** per definire l’elenco di colonne alle quali viene applicata la riconciliazione dei dati."

Nell’attività **[!UICONTROL Combina]**, puoi configurare un’**[!UICONTROL Intersezione]**. A questo scopo, segui i passaggi aggiuntivi riportati di seguito:

1. Seleziona il **[!UICONTROL Tipo di riconciliazione]** per definire la modalità di gestione dei duplicati. Consulta la sezione [Unione](#union).
1. Puoi selezionare l’opzione **[!UICONTROL Genera complemento]** se desideri elaborare la popolazione rimanente. Il complemento conterrà l’unione dei risultati di tutte le attività in entrata senza l’intersezione. Verrà quindi aggiunta all’attività un’ulteriore transizione in uscita.

L&#39;esempio seguente mostra l&#39;**[!UICONTROL intersezione]** tra due attività di query. Viene utilizzato qui per recuperare profili con un’iscrizione fedeltà il cui ultimo acquisto è stato effettuato meno di un mese fa.

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

1. Nella sezione **[!UICONTROL Set da unire]**, dalle transizioni in entrata, seleziona **[!UICONTROL Set primario]**. Questo è il set da cui gli elementi sono esclusi. Gli altri set confrontano gli elementi prima che vengano esclusi dal set primario.
1. Se necessario, è possibile elaborare le tabelle in entrata. In effetti, per escludere un target da un’altra dimensione, tale target deve essere restituito nella stessa dimensione targeting del target principale. A questo scopo, nella sezione **[!UICONTROL Regole di esclusione]**, fai clic su **[!UICONTROL Aggiungi una regola]** e specifica le condizioni per la modifica delle dimensioni. La riconciliazione dei dati viene eseguita tramite un attributo o un’unione.
1. Puoi selezionare l’opzione **[!UICONTROL Genera complemento]** se desideri elaborare la popolazione rimanente. Consulta la sezione [Intersezione](#intersection).

L&#39;esempio di **[!UICONTROL esclusione]** seguente mostra due query configurate per filtrare i profili che hanno acquistato un prodotto. I profili che non hanno un’iscrizione fedeltà vengono quindi esclusi dal primo set.

Perché: stai conducendo una campagna di fidelizzazione, quindi i non membri sono irrilevanti.

![](../assets/orchestrated-exclusion-example.png)

