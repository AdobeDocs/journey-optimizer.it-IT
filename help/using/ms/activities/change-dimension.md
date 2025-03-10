---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Modifica dimensione
description: Scopri come utilizzare l’attività Modifica dimensione
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
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

L’attività **Cambia dimensione** è un’attività di **targeting**. Questa attività ti consente di modificare la dimensione di targeting durante la creazione di una campagna in più passaggi. Sposta l’asse in base al modello di dati e alla dimensione di input.

Ad esempio, puoi passare la dimensione di targeting di una campagna con più passaggi da &quot;Destinatari&quot; a &quot;Applicazione abbonati&quot; per inviare notifiche push ai destinatari interessati.

>[!IMPORTANT]
>
>Le attività **[!UICONTROL Modifica dimensione]** e **[!UICONTROL Modifica origine dati]** non devono essere aggiunte in una riga. Se devi utilizzare entrambe le attività consecutivamente, assicurati di includere un&#39;attività **[!UICONTROL Arricchimento]** tra di esse. In questo modo si garantisce la corretta esecuzione e si evitano potenziali conflitti o errori.

## Configurare l’attività Cambia dimensione {#configure}

Per configurare l’attività **Cambia dimensione** segui questi passaggi:

1. Aggiungi un&#39;attività **Modifica dimensione** alla campagna in più passaggi.

   ![](../assets/workflow-change-dimension.png)

1. Definisci la **Nuova dimensione target**. Durante la modifica della dimensione, tutti i record vengono mantenuti. Altre opzioni non sono ancora disponibili.

1. Esegui la campagna in più passaggi per visualizzare il risultato. Confronta i dati nelle tabelle prima e dopo l’attività di modifica della dimensione e confronta la struttura delle tabelle delle campagne in più passaggi.

## Esempio {#example}

In questo esempio, si desidera inviare una consegna SMS a tutti i profili che hanno effettuato un acquisto. A questo scopo, viene prima utilizzata un’ attività **[!UICONTROL Creazione del pubblico]** collegata a una dimensione targeting “Acquisto” personalizzata per eseguire il targeting di tutti gli acquisti effettuati.

Quindi utilizziamo un&#39;attività **[!UICONTROL Modifica dimensione]** per cambiare la dimensione di targeting di una campagna in più passaggi in &quot;Destinatari&quot;. Questo consente di eseguire il targeting dei destinatari che corrispondono alla query.

![](../assets/workflow-change-dimension-example.png)
