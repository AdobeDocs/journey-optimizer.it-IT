---
solution: Journey Optimizer
product: journey optimizer
title: Modificare o interrompere una campagna
description: Scopri come modificare, interrompere o duplicare le campagne live in Journey Optimizer
Feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: gestire campagne, stato, pianificazione, accesso, ottimizzatore
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 3f96cc0037b5bcdb2ce94e2721b02ba13b3cff36
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---

# Gestire le campagne {#modify-stop-campaign}

Una volta attivata una campagna, puoi modificarla o interromperla in qualsiasi momento. Queste operazioni sono disponibili solo per le campagne con un’esecuzione ricorrente.

Inoltre, puoi duplicare le campagne live (eseguite una volta o con un’esecuzione ricorrente) per crearne di nuove e archiviare le campagne completate o interrotte.

## Accedere alle campagne {#access}

Le campagne sono accessibili dalla **[!UICONTROL Campagne]** menu.

Per impostazione predefinita, l’elenco mostra tutte le campagne con **[!UICONTROL Bozza]**, **[!UICONTROL Pianificato]**, e **[!UICONTROL Live]** stati. Per visualizzare le campagne interrotte, completate e archiviate, è necessario cancellare il filtro.

![](assets/create-campaign-list.png)

Inoltre, puoi filtrare l’elenco in base al tipo di campagna e al canale, o ai tag assegnati alle campagne durante la loro creazione. [Scopri come assegnare tag a una campagna](create-campaign.md#create)

## Stati delle campagne {#statuses}

Le campagne possono avere più stati:

* **[!UICONTROL Bozza]**: la campagna è in fase di modifica e non è stata attivata.
* **[!UICONTROL Attivazione]**: attivazione della campagna in corso.
* **[!UICONTROL Live]**: la campagna è stata attivata.
* **[!UICONTROL Pianificato]**: la campagna è configurata per essere attivata in una data di inizio specifica.
* **[!UICONTROL Interrotto]**: la campagna è stata interrotta manualmente. Non è più possibile attivarla o riutilizzarla. [Scopri come interrompere una campagna](modify-stop-campaign.md#stop)
* **[!UICONTROL Completato]**: campagna completata. Questo stato viene assegnato automaticamente 3 giorni dopo l’attivazione di una campagna o alla data di fine della campagna, se questa ha un’esecuzione ricorrente.
* **[!UICONTROL Archiviato]**: la campagna è stata archiviazione. [Scopri come archiviare le campagne](modify-stop-campaign.md#archive)

>[!NOTE]
>
>L’icona &quot;Apri versione bozza&quot; accanto a una **[!UICONTROL Live]** o **[!UICONTROL Pianificato]** Lo stato indica che è stata creata una nuova versione della campagna, che non è ancora stata attivata. [Ulteriori informazioni](modify-stop-campaign.md#modify).

## Modificare una campagna ricorrente {#modify}

Per modificare e creare una nuova versione di una campagna ricorrente, effettua le seguenti operazioni:

1. Apri la campagna, quindi fai clic su **[!UICONTROL Modifica campagna]** pulsante.

1. Viene creata una nuova versione della campagna. Puoi controllare la versione live facendo clic su **[!UICONTROL Apri versione live]**.

   ![](assets/create-campaign-draft.png)

   Nell’elenco delle campagne, le campagne attivate con una versione bozza in corso vengono visualizzate con un’icona specifica nella sezione **[!UICONTROL Stato]** colonna. Fai clic su questa icona per aprire la versione bozza della campagna.

   ![](assets/create-campaign-edit-list.png)

1. Quando le modifiche sono pronte, puoi attivare la nuova versione della campagna (vedi [Rivedere e attivare una campagna](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >L’attivazione della bozza sostituirà la versione live della campagna.

## Interrompere una campagna ricorrente {#stop}

Per interrompere una campagna ricorrente, aprila e fai clic su **[!UICONTROL Interrompi campagna]** pulsante.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>L’interruzione di una campagna non interrompe un invio in corso, ma interrompe un invio pianificato o le occorrenze successive se l’invio è già in corso.

<!-- inbound campaign (inapp): can stop and resume -->

## Duplicare una campagna {#duplicate}

Puoi duplicare una campagna live per crearne una nuova. A questo scopo, apri la campagna, quindi fai clic su **[!UICONTROL Duplica]**.

![](assets/create-campaign-duplicate.png)

## Archiviare una campagna {#archive}

Con il tempo, l’elenco delle campagne continua a crescere e alla fine diventa più difficile sfogliare le campagne completate e interrotte.

Per evitare questo problema, puoi archiviare campagne completate e interrotte che non sono più necessarie. A questo scopo, fai clic sul pulsante con i puntini di sospensione, quindi seleziona **[!UICONTROL Archivia]**.

![](assets/create-campaign-archive.png)

Le campagne archiviate possono quindi essere recuperate utilizzando il filtro dedicato nell’elenco. [Scopri come accedere alle campagne](get-started-with-campaigns.md#access)
