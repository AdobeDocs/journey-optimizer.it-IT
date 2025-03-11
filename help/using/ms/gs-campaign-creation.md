---
solution: Journey Optimizer
product: journey optimizer
title: Principi chiave della creazione di campagne in più passaggi
description: Scopri i principi chiave delle campagne in più passaggi con Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 326a0a47c859f475d9036c6142b057a5b59b0ae9
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 24%

---

# Principi chiave della campagna orchestrata {#ms-campaign-creation}

>[!CONTEXTUALHELP]
>id="ajo_targeting_workflow_list"
>title="Campagna in più passaggi"
>abstract="In questa schermata, puoi accedere all’elenco completo delle campagne con più passaggi, controllarne lo stato corrente, le date dell’ultima/successiva esecuzione e creare una nuova campagna con più passaggi."

Con Adobe Journey Optimizer, puoi creare campagne con più passaggi in un’area di lavoro visiva per progettare processi cross-channel come segmentazione, esecuzione di campagne, elaborazione di file.

## Cosa c&#39;è all&#39;interno di una campagna in più passaggi? {#gs-ms-campaign-inside}

L’area di lavoro della campagna in più passaggi è una rappresentazione di ciò che dovrebbe accadere. Descrive le varie attività da eseguire e il modo in cui vengono collegate tra loro.

![](assets/workflow-example.png){zoomable="yes"} {zoomable="yes"}

Ogni campagna in più passaggi contiene:

* **Attività**: un’attività è un’attività da eseguire. Le varie attività disponibili sono rappresentate nel diagramma tramite icone. Ogni attività presenta proprietà specifiche e altre proprietà comuni a tutte le attività.

  In un diagramma di una campagna in più passaggi, una determinata attività può produrre più attività, in particolare quando si verifica un ciclo continuo o azioni ricorrenti.

* **Transizioni**: le transizioni collegano un’attività di origine a un’attività di destinazione e ne definiscono la sequenza.

* **Tabelle di lavoro**: la tabella di lavoro contiene tutte le informazioni riportate dalla transizione. Ogni campagna con più passaggi utilizza diverse tabelle di lavoro. I dati trasmessi in queste tabelle possono essere utilizzati in tutto il ciclo di vita della campagna in più fasi.

## Passaggi chiave per creare una campagna in più passaggi {#gs-ms-campaign-steps}

I passaggi chiave per creare una campagna in più passaggi sono i seguenti:

![](assets/workflow-creation-process.png){zoomable="yes"}

## Accedere alle campagne in più passaggi

Nel menu **[!UICONTROL Campagne]**, passa alla scheda Più passaggi per accedere all&#39;elenco completo delle campagne con più passaggi.

Ogni campagna in più passaggi nell&#39;elenco visualizza informazioni sul suo [stato](#status) corrente, sull&#39;ultima volta che è stata eseguita o modificata e sulla data e ora di esecuzione pianificate successive.

Puoi personalizzare le colonne visualizzate facendo clic sull’icona **[!UICONTROL Configura le colonne per un layout personalizzato]**, nell’angolo superiore a destra dell’elenco. Ciò ti consente di aggiungere ulteriori informazioni all’elenco, ad esempio l’ultima attività in errore per ogni campagna con più passaggi o la dimensione di targeting applicata.

Inoltre, sono disponibili una barra di ricerca e dei filtri per facilitare la ricerca all’interno dell’elenco. Ad esempio, puoi filtrare le campagne in più passaggi per visualizzare solo quelle appartenenti a una campagna o quelle elaborate durante un intervallo di date specifico.

Per duplicare o eliminare una campagna con più passaggi, fai clic sul pulsante con i puntini di sospensione, quindi seleziona **[!UICONTROL Duplica]** o **[!UICONTROL Elimina]**.

>[!NOTE]
>
>Quando è in corso una campagna con più passaggi, puoi duplicarla, ma non eliminarla.

## Stati e ciclo di vita {#status}

Le campagne possono avere più stati:

* **[!UICONTROL Bozza]**: la campagna con più passaggi è stata creata e salvata.
* **[!UICONTROL In corso]**: la campagna con più passaggi è attualmente in esecuzione.
* **[!UICONTROL Completata]**: esecuzione della campagna in più passaggi completata.
* **[!UICONTROL Sospeso]**: la campagna con più passaggi è stata sospesa.
* **[!UICONTROL Errore]**: la campagna con più passaggi ha rilevato un errore. Apri la campagna in più passaggi e accedi ai registri e alle attività per identificare l’errore e risolverlo.


## Creare una query

## Linee guida di Personalization
