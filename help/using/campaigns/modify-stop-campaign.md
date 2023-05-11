---
solution: Journey Optimizer
product: journey optimizer
title: Modificare o interrompere una campagna
description: Scopri come modificare, interrompere o duplicare campagne live in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: gestire campagne, stato, pianificazione, accesso, ottimizzatore
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '520'
ht-degree: 2%

---

# Gestire le campagne {#modify-stop-campaign}

Una volta attivata una campagna, puoi modificarla o interromperla in qualsiasi momento. Queste operazioni sono disponibili solo per le campagne con esecuzione ricorrente .

Inoltre, puoi duplicare le campagne live (eseguite una volta o con un’esecuzione ricorrente) per crearne di nuove e archiviare quelle completate o interrotte.

## Accedere alle campagne {#access}

Le campagne sono accessibili dal **[!UICONTROL Campagne]** menu.

Per impostazione predefinita, l’elenco mostra tutte le campagne con **[!UICONTROL Bozza]**, **[!UICONTROL Pianificato]** e **[!UICONTROL Live]** stati. Per visualizzare le campagne interrotte, completate e archiviate, devi cancellare il filtro.

![](assets/create-campaign-list.png)

Inoltre, puoi filtrare l’elenco in base al tipo di campagna e al canale, o ai tag assegnati alle campagne al momento della loro creazione. [Scopri come assegnare tag a una campagna](create-campaign.md#create)

## Stati di Campaign {#statuses}

Le campagne possono avere più stati:

* **[!UICONTROL Bozza]**: La campagna è in corso di modifica e non è stata attivata.
* **[!UICONTROL Attivazione]**: È in corso l’attivazione della campagna.
* **[!UICONTROL Live]**: La campagna è stata attivata.
* **[!UICONTROL Pianificato]**: La campagna è configurata per essere attivata in una data di inizio specifica.
* **[!UICONTROL Arrestato]**: La campagna è stata arrestata manualmente. Non è più possibile attivarlo o riutilizzarlo. [Scopri come interrompere una campagna](modify-stop-campaign.md#stop)
* **[!UICONTROL Completato]**: La campagna è completa. Questo stato viene assegnato automaticamente 3 giorni dopo l’attivazione di una campagna oppure alla data di fine della campagna, se presenta un’esecuzione ricorrente.
* **[!UICONTROL Archiviato]**: La campagna è stata archiviata. [Scopri come archiviare le campagne](modify-stop-campaign.md#archive)

>[!NOTE]
>
>Icona &quot;Apri versione bozza&quot; accanto a una **[!UICONTROL Live]** o **[!UICONTROL Pianificato]** lo stato indica che è stata creata una nuova versione della campagna e che non è ancora stata attivata. [Maggiori informazioni](modify-stop-campaign.md#modify).

## Modificare una campagna ricorrente {#modify}

Per modificare e creare una nuova versione di una campagna ricorrente, effettua le seguenti operazioni:

1. Apri la campagna e fai clic su **[!UICONTROL Modifica campagna]** pulsante .

1. Viene creata una nuova versione della campagna. Per controllare la versione attiva, fai clic su **[!UICONTROL Open live version]**.

   ![](assets/create-campaign-draft.png)

   Nell’elenco delle campagne, le campagne attivate con una versione bozza in corso vengono visualizzate con un’icona specifica nel **[!UICONTROL Stato]** colonna. Fai clic su questa icona per aprire la versione bozza della campagna.

   ![](assets/create-campaign-edit-list.png)

1. Una volta pronte le modifiche, puoi attivare la nuova versione della campagna (vedi [Rivedere e attivare una campagna](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >L’attivazione della bozza sostituirà la versione live della campagna.

## Interrompere una campagna ricorrente {#stop}

Per interrompere una campagna ricorrente, aprilo e fai clic sul pulsante **[!UICONTROL Interrompi campagna]** pulsante .

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>L’arresto di una campagna non interrompe l’invio in corso, ma interrompe l’invio pianificato o le occorrenze successive, se l’invio è già in corso.

<!-- inbound campaign (inapp): can stop and resume -->

## Duplicare una campagna {#duplicate}

Puoi duplicare una campagna live per crearne una nuova. A questo scopo, apri la campagna, quindi fai clic su **[!UICONTROL Duplica]**.

![](assets/create-campaign-duplicate.png)

## Archiviare una campagna {#archive}

Con il tempo, l&#39;elenco delle campagne continua a crescere e alla fine rende più difficile sfogliare le campagne completate e interrotte.

Per evitare questo problema, puoi archiviare le campagne completate e interrotte di cui non hai più bisogno. A questo scopo, fai clic sul pulsante dei puntini di sospensione e seleziona **[!UICONTROL Archivia]**.

![](assets/create-campaign-archive.png)

Le campagne archiviate possono quindi essere recuperate utilizzando il filtro dedicato presente nell’elenco. [Scopri come accedere alle campagne](get-started-with-campaigns.md#access)
