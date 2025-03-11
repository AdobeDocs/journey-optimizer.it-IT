---
solution: Journey Optimizer
product: journey optimizer
title: Principi chiave della creazione di campagne in più passaggi
description: Scopri i principi chiave delle campagne in più passaggi con Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: b04aa15a-71bf-4683-bcbf-f611c189ffe1
source-git-commit: 271c4739a5537a99da981913606bc9eb099b5139
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 27%

---

# Principi chiave della campagna orchestrata {#ms-campaign-creation}

Con Adobe Journey Optimizer, puoi creare campagne con più passaggi in un’area di lavoro visiva per progettare processi cross-channel come segmentazione, esecuzione di campagne, elaborazione di file.

## Creare una query

## Linee guida di Personalization

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

## Stati e ciclo di vita

Le campagne possono avere più stati:

* **[!UICONTROL Bozza]**: la campagna con più passaggi è stata creata e salvata.
* **[!UICONTROL In corso]**: la campagna con più passaggi è attualmente in esecuzione.
* **[!UICONTROL Completata]**: esecuzione della campagna in più passaggi completata.
* **[!UICONTROL Sospeso]**: la campagna con più passaggi è stata sospesa.
* **[!UICONTROL Errore]**: la campagna con più passaggi ha rilevato un errore. Apri la campagna in più passaggi e accedi ai registri e alle attività per identificare l’errore e risolverlo.

