---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Modifica dimensione
description: Scopri come utilizzare l’attività Modifica dimensione
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 94de60c33c7cf1d8956294aebb91d7533534088f
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 45%

---

# Cambiare dimensione {#change-dimension}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_dimension_complement"
>title="Generare un complemento"
>abstract="Puoi generare una transizione in uscita aggiuntiva con la popolazione rimanente, che è stata esclusa come duplicato. A tale scopo, attiva l’opzione **Genera complemento**"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_change_dimension"
>title="Attività Cambia dimensione"
>abstract="Questa attività ti consente di modificare la dimensione targeting durante la creazione di un pubblico. Sposta l’asse in base al modello di dati e alla dimensione di input. Ad esempio, puoi passare dalla dimensione “contratti” alla dimensione “clienti”."

In qualità di addetto al marketing, puoi cambiare la dimensione di targeting da un’entità a un’altra entità collegata all’interno di una campagna orchestrata e perfezionare il targeting del pubblico in base a set di dati diversi, ad esempio passando dal profiling degli utenti al targeting di azioni o prenotazioni specifiche.

Per eseguire questa operazione, utilizzare l&#39;attività di targeting **Modifica dimensione**. Questa attività ti consente di modificare la dimensione di targeting durante la creazione della campagna orchestrata. Sposta l’asse in base al modello di dati e alla dimensione di input.

Ad esempio, puoi cambiare la dimensione di targeting di una campagna orchestrata da &quot;Profilo&quot; a &quot;Contratti&quot; per inviare messaggi al proprietario del contratto di destinazione.

<!--
>[!IMPORTANT]
>
>Please note that the **[!UICONTROL Change Dimension]** and **[!UICONTROL Change Data source]** activities should not be added in one row. If you need to use both activities consecutively, make sure you include an **[!UICONTROL Enrichement]** activity in between them. This ensures proper execution and prevents potential conflicts or errors.-->

## Configurare l’attività Cambia dimensione {#configure}

Per configurare l’attività **Cambia dimensione** segui questi passaggi:

1. Aggiungi un&#39;attività **Modifica dimensione** alla campagna orchestrata.

   ![](../assets/change-dimension.png)

1. Definisci la **Nuova dimensione target**. Durante la modifica della dimensione vengono conservati tutti i record.

1. Esegui la campagna orchestrata per visualizzare il risultato. Confronta i dati nelle tabelle prima e dopo l’attività di modifica della dimensione e confronta la struttura delle tabelle delle campagne orchestrate.

## Esempio {#example}

In questo esempio, si desidera inviare una consegna SMS a tutti i profili che hanno effettuato un acquisto. A questo scopo, viene prima utilizzata un’ attività **[!UICONTROL Creazione del pubblico]** collegata a una dimensione targeting “Acquisto” personalizzata per eseguire il targeting di tutti gli acquisti effettuati.

Quindi utilizziamo un&#39;attività **[!UICONTROL Change dimension]** per cambiare la dimensione di targeting della campagna orchestrata in &quot;Recipients&quot;. Questo consente di eseguire il targeting dei destinatari che corrispondono alla query.

![](../assets/change-dimension-example.png)
