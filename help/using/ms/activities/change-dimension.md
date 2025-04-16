---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Modifica dimensione
description: Scopri come utilizzare l’attività Modifica dimensione
hide: true
hidefromtoc: true
exl-id: 83e66f10-93dd-4759-840c-2c83abc42a28
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 50%

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

L’attività **Cambia dimensione** è un’attività di **targeting**. Questa attività ti consente di modificare la dimensione di targeting durante la creazione della campagna orchestrata. Sposta l’asse in base al modello di dati e alla dimensione di input.

Ad esempio, puoi cambiare la dimensione di targeting di una campagna orchestrata da &quot;Destinatari&quot; a &quot;Applicazione abbonati&quot; per inviare notifiche push ai destinatari target.

>[!IMPORTANT]
>
>Le attività **[!UICONTROL Modifica dimensione]** e **[!UICONTROL Modifica origine dati]** non devono essere aggiunte in una riga. Se devi utilizzare entrambe le attività consecutivamente, assicurati di includere un&#39;attività **[!UICONTROL Arricchimento]** tra di esse. In questo modo si garantisce la corretta esecuzione e si evitano potenziali conflitti o errori.

## Configurare l’attività Cambia dimensione {#configure}

Per configurare l’attività **Cambia dimensione** segui questi passaggi:

1. Aggiungi un&#39;attività **Modifica dimensione** alla campagna orchestrata.

   ![](../assets/workflow-change-dimension.png)

1. Definisci la **Nuova dimensione target**. Durante la modifica della dimensione, tutti i record vengono mantenuti. Altre opzioni non sono ancora disponibili.

1. Esegui la campagna orchestrata per visualizzare il risultato. Confronta i dati nelle tabelle prima e dopo l’attività di modifica della dimensione e confronta la struttura delle tabelle delle campagne orchestrate.

## Esempio {#example}

In questo esempio, si desidera inviare una consegna SMS a tutti i profili che hanno effettuato un acquisto. A questo scopo, viene prima utilizzata un’ attività **[!UICONTROL Creazione del pubblico]** collegata a una dimensione targeting “Acquisto” personalizzata per eseguire il targeting di tutti gli acquisti effettuati.

Quindi utilizziamo un&#39;attività **[!UICONTROL Change dimension]** per cambiare la dimensione di targeting della campagna orchestrata in &quot;Recipients&quot;. Questo consente di eseguire il targeting dei destinatari che corrispondono alla query.

![](../assets/workflow-change-dimension-example.png)
