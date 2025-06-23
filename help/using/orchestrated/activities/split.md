---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività di suddivisione
description: Scopri come utilizzare l’attività Split in una campagna orchestrata
badge: label="Alfa"
hide: true
hidefromtoc: true
exl-id: 986bc566-123a-451d-a4a6-bbf5a2798849
source-git-commit: 38b65200435e0b997e79aefbb66549b9168188fd
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 54%

---

# Dividi {#split}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split"
>title="Attività Dividi"
>abstract="L’attività **Dividi** consente di segmentare le popolazioni in ingresso in più sottoinsiemi in base a criteri di selezione diversi, ad esempio le regole di filtro o le dimensioni della popolazione."

+++ Sommario

| Benvenuto in campagne orchestrate | Lanciare la prima campagna orchestrata | Eseguire query sul database | Attività di campagne orchestrate |
|---|---|---|---|
| [Introduzione alle campagne orchestrate](../gs-orchestrated-campaigns.md)<br/><br/>[Passaggi di configurazione](../configuration-steps.md)<br/><br/>[Passaggi chiave per la creazione di campagne orchestrate](../gs-campaign-creation.md) | [Creare una campagna orchestrata](../create-orchestrated-campaign.md)<br/><br/>[Orchestrare le attività](../orchestrate-activities.md)<br/><br/>[Inviare messaggi con le campagne orchestrate](../send-messages.md)<br/><br/>[Avviare e monitorare la campagna](../start-monitor-campaigns.md)<br/><br/>[Generazione rapporti](../reporting-campaigns.md) | [Utilizzare Query Modeler](../orchestrated-rule-builder.md)<br/><br/>[Creare la prima query](../build-query.md)<br/><br/>[Modificare le espressioni](../edit-expressions.md) | [Inizia a usare le attività](about-activities.md)<br/><br/>Attività:<br/>[Partecipa/Partecipa](and-join.md) - [Genera pubblico](build-audience.md) - [Modifica dimensione](change-dimension.md) - [Combina](combine.md) - [Deduplicazione](deduplication.md) - [Arricchimento](enrichment.md) - [Fork](fork.md) - [Riconciliazione](reconciliation.md) - [Dividi](split.md) - [Attendi](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

L&#39;attività **[!UICONTROL Split]** è un&#39;attività **[!UICONTROL Targeting]** che segmenta il gruppo in ingresso in più sottoinsiemi in base a criteri di selezione definiti, ad esempio regole di filtro o dimensioni del gruppo.

## Configurare l’attività Dividi {#split-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_segments"
>title="Segmenti per attività Dividi"
>abstract="Aggiungi tutti i sottoinsiemi desiderati per segmentare la popolazione in ingresso.<br/></br>Quando viene eseguita l’attività **Dividi**, la popolazione viene segmentata tra i diversi sottoinsiemi nell’ordine in cui vengono aggiunti all’attività. Prima di avviare la campagna orchestrata, assicurati di aver ordinato i sottoinsiemi nell’ordine più adatto alle tue esigenze utilizzando i pulsanti freccia."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_filter"
>title="Filtro attività Dividi"
>abstract="Per applicare una condizione di filtro al sottoinsieme, fai clic su **[!UICONTROL Crea filtro]** e configura la regola di filtro desiderata utiizzando il query modeler. Ad esempio, includi i profili della popolazione in ingresso il cui indirizzo e-mail esiste nel database."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_limit"
>title="Limite attività Dividi"
>abstract="Per limitare il numero di profili selezionati dal sottoinsieme, attiva l’opzione **[!UICONTROL Abilita limite]** e specifica il numero o le percentuali della popolazione da includere."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_sorting"
>title="Ordinamento attività Dividi"
>abstract="Quando imposti un limite di popolazione per un sottoinsieme, puoi classificare i profili selezionati in base a un attributo di profilo specifico, in ordine crescente o decrescente. A tale scopo, attiva l’opzione **Abilita ordinamento**. Ad esempio, puoi limitare un sottoinsieme in modo da includere solo i primi 50 profili con l’importo di acquisto più alto."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_complement"
>title="Complemento generato da suddivisione"
>abstract="Dopo aver configurato tutti i sottoinsiemi, puoi selezionare la popolazione rimanente che non corrisponde a nessuno dei sottoinsiemi e includerli in un’ulteriore transizione in uscita. A tale scopo, attiva l’opzione **Genera complemento**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_generatesubsets"
>title="Generare tutti i sottoinsiemi nella stessa tabella"
>abstract="Attiva questa opzione per raggruppare tutti i sottoinsiemi in una singola transizione di output."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_emptytransition"
>title="Ignora transizione vuota"
>abstract="Attiva l’opzione **[!UICONTROL Ignora transizione vuota]** per disabilitare la transizione di output per questo sottoinsieme se la popolazione in ingresso è vuota."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_split_enable_overlapping"
>title="Abilita sovrapposizione popolazioni di output"
>abstract=" L’opzione **[!UICONTROL Abilita sovrapposizione popolazioni di output]** consente di gestire le popolazioni appartenenti a diversi sottoinsiemi. Quando questa opzione non è selezionata, l’attività Dividi si assicura che un destinatario non possa essere presente in diverse transizioni di output, anche se soddisfa i criteri di diversi sottoinsiemi. Saranno nella destinazione della prima scheda con i criteri corrispondenti. Quando questa opzione è selezionata, i destinatari possono essere in più sottoinsiemi se soddisfano i rispettivi criteri di filtro."

Per configurare l’attività **[!UICONTROL Dividi]** segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Dividi]** alla campagna orchestrata.

1. Il riquadro di configurazione dell’attività si apre con un sottoinsieme predefinito. Fai clic sul pulsante **[!UICONTROL Aggiungi segmento]** per aggiungere tutti i sottoinsiemi desiderati per segmentare la popolazione in ingresso.

   ![](../assets/orchestrated-split-1.png)

   >[!IMPORTANT]
   >
   >L&#39;attività **Split** elabora i sottoinsiemi nell&#39;ordine in cui vengono aggiunti. Ad esempio, se il primo sottoinsieme acquisisce il 70% della popolazione, il successivo applica i propri criteri al restante 30%.
   >
   >Prima di eseguire la campagna orchestrata, assicurati che i sottoinsiemi siano ordinati come previsto. Utilizzare i pulsanti freccia per regolarne la posizione.

1. Una volta aggiunti i sottoinsiemi, l’attività mostra tante transizioni di output quanti sono i sottoinsiemi. Consigliamo vivamente di modificare l’etichetta di ciascun sottoinsieme per identificarlo facilmente nell’area di lavoro orchestrata della campagna.

1. Configura i filtri per ciascun sottoinsieme:

   1. Fare clic su un sottoinsieme per aprirne le impostazioni.

   1. Fare clic su **[!UICONTROL Crea filtro]** per definire le regole di filtro mediante il modellatore di query, ad esempio per selezionare profili con un indirizzo e-mail valido.

      ![](../assets/orchestrated-split-1.png)

   1. Per limitare il numero di profili selezionati, abilitare **[!UICONTROL Abilita limite]** e specificare un numero o una percentuale.

   1. Per ignorare una transizione quando il sottoinsieme è vuoto, abilitare **[!UICONTROL Ignora transizione vuota].**

1. Per includere profili non corrispondenti a un sottoinsieme, abilitare **[!UICONTROL Genera complemento]**. Questo crea una transizione in uscita aggiuntiva per la popolazione rimanente.

   >[!NOTE]
   >
   >Abilita **[!UICONTROL Genera tutti i sottoinsiemi nella stessa tabella]** per raggruppare tutti i sottoinsiemi in un&#39;unica transizione.

1. Utilizza **[!UICONTROL Abilita la sovrapposizione delle popolazioni di output]** per consentire la visualizzazione dei profili in più sottoinsiemi:

   * **Se non è selezionato**, ogni profilo viene assegnato a un solo sottoinsieme, il primo di cui corrisponde i criteri anche se è idoneo per altri sottoinsiemi.

   * **Se selezionato**, i profili possono essere inclusi in più sottoinsiemi se soddisfano i criteri per ciascuno di essi.

L’attività adesso è configurata. Al momento dell’esecuzione della campagna orchestrata, la popolazione verrà segmentata in diversi sottoinsiemi, nell’ordine in cui sono stati aggiunti all’attività.

## Esempio{#split-example}

Nell’esempio seguente, l’attività **[!UICONTROL Dividi]** viene utilizzata per segmentare un pubblico in sottoinsiemi distinti in base al canale di comunicazione che si desidera utilizzare:

* **Sottoinsieme 1 &quot;email&quot;**: include i profili che hanno fornito un numero di telefono.

* **Sottoinsieme 2 &quot;sms&quot;**: esegue il targeting dei profili con un numero di telefono cellulare archiviato nel database.

* **Transizione complemento**: acquisisce tutti i profili rimanenti che non soddisfano i criteri per nessuno dei sottoinsiemi.

![](../assets/orchestrated-split-3.png)
