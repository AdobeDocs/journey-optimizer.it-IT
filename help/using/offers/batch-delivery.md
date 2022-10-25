---
title: Batch Decisioning
description: Scopri come distribuire le decisioni sulle offerte a tutti i profili in un dato segmento Adobe Experience Platform.
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
source-git-commit: f3f38e7db95bd1a6dc41b1626177c800280fb71c
workflow-type: tm+mt
source-wordcount: '814'
ht-degree: 2%

---

# Batch Decisioning {#deliver}

## Guida introduttiva alle decisioni in batch {#start}

Journey Optimizer ti consente di fornire le decisioni sulle offerte a tutti i profili in un dato segmento Adobe Experience Platform.

A questo scopo, devi creare una richiesta di lavoro in Journey Optimizer che conterrà informazioni sul segmento di cui eseguire il targeting e sulla decisione di utilizzare l’offerta. Il contenuto dell’offerta per ciascun profilo del segmento viene quindi inserito in un set di dati Adobe Experience Platform, dove è disponibile per flussi di lavoro batch personalizzati.

La distribuzione in batch può essere eseguita anche utilizzando le API. Per ulteriori informazioni, consulta la sezione [Documentazione API di Batch Decisioning](api-reference/offer-delivery-api/batch-decisioning-api.md).

## Prerequisiti {#prerequisites}

Prima di configurare una richiesta di lavoro, assicurati di aver creato:

* **Un set di dati** in Adobe Experience Platform. Questo set di dati verrà utilizzato per memorizzare il risultato della decisione utilizzando lo schema &quot;ODE DecisionEvents&quot;. Ulteriori informazioni nel [Documentazione dei set di dati](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=it).

* **Un segmento** in Adobe Experience Platform. Il segmento deve essere valutato e quindi aggiornato. Scopri come aggiornare la valutazione dell’appartenenza al segmento nel [Documentazione del servizio di segmentazione](http://www.adobe.com/go/segmentation-overview-en)

   >[!NOTE]
   >
   >Un processo batch viene eseguito fuori dallo snapshot del profilo che si verifica una volta al giorno. Le decisioni in batch limitano la frequenza e caricano sempre i profili dallo snapshot più recente.

* **Una decisione** in Adobe Journey Optimizer. [Scopri come creare una decisione](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## Creare una richiesta di lavoro

Per creare una nuova richiesta di lavoro, segui la procedura seguente.

1. In **[!UICONTROL Offerte]** aprire il menu **[!UICONTROL Decisioni in batch]** scheda e fai clic su **[!UICONTROL Crea richiesta]**.

   ![](assets/batch-create.png)

1. Denomina la richiesta di lavoro, quindi seleziona il set di dati in cui devono essere inviati i dati del processo.

1. Seleziona il segmento Adobe Experience Platform di cui eseguire il targeting.

1. Seleziona uno o più ambiti decisionali dell’offerta che desideri utilizzare per consegnare le offerte al segmento:
   1. Seleziona un posizionamento dall’elenco.
   1. Vengono visualizzate le decisioni disponibili per il posizionamento selezionato. Seleziona la scelta e fai clic su **[!UICONTROL Aggiungi]**.
   1. Ripeti l’operazione per aggiungere tutti gli ambiti decisionali desiderati.

   ![](assets/batch-decision.png)

1. Per impostazione predefinita, viene restituita un’offerta dell’ambito decisionale per ciascun profilo. Puoi regolare il numero di offerte restituite utilizzando la **[!UICONTROL Richiesta di offerta per profilo]** opzione . Ad esempio, se selezioni 2, verranno visualizzate le migliori 2 offerte per l’ambito di decisione selezionato.

   >[!NOTE]
   >
   >Puoi richiedere fino a 30 offerte per ambito decisionale.

1. Se desideri includere il contenuto dell’offerta nel set di dati, attiva l’opzione **[!UICONTROL Includi contenuto]** su . Questa opzione è disabilitata per impostazione predefinita.

1. Fai clic su **[!UICONTROL Crea]** per eseguire la richiesta di lavoro.

## Monitorare i processi batch

Tutti i processi batch richiesti sono accessibili dal **[!UICONTROL Decisioni in batch]** scheda . Sono inoltre disponibili strumenti di ricerca e filtro per facilitare la definizione dell’elenco.

![](assets/batch-list.png)

### Stato richieste processo

Una volta creata una richiesta di processo, il processo batch attraversa più stati:

>[!NOTE]
>
>Per ottenere le informazioni più recenti sullo stato di una richiesta di lavoro, utilizza il pulsante di sospensione accanto al processo per aggiornarlo.

1. **[!UICONTROL In coda]**: La richiesta di processo è stata creata ed è entrata nella coda di elaborazione. È possibile eseguire fino a 5 processi batch alla volta per set di dati. Eventuali altre richieste batch con lo stesso set di dati di output vengono aggiunte alla coda. Un processo in coda viene raccolto per l&#39;elaborazione una volta che il processo precedente è stato completato.
1. **[!UICONTROL Elaborazione]**: Elaborazione della richiesta di processo in corso
1. **[!UICONTROL Acquisizione]**: La richiesta del processo è stata eseguita. I dati dei risultati vengono acquisiti nel set di dati selezionato,
1. **[!UICONTROL Completato]**: La richiesta del processo è stata eseguita e i dati dei risultati sono ora memorizzati nel set di dati selezionato.

   >[!NOTE]
   >
   >Per accedere al set di dati in cui vengono memorizzati i risultati di un processo, fai clic sul relativo nome nell’elenco dei processi.

Se si verifica un errore durante l’esecuzione della richiesta di processo, riceverà il **[!UICONTROL Errore]** stato. Prova a duplicare il processo batch per creare una nuova richiesta. [Scopri come duplicare un processo batch](#duplicate)

### Tempo di elaborazione del processo batch

L&#39;ora end-to-end per ogni processo batch è la durata dal momento in cui il carico di lavoro viene creato al momento in cui il risultato della decisione è disponibile nel set di dati di output.

La dimensione del segmento è il fattore principale che influisce sul tempo di decisione del batch end-to-end. Se l’offerta idonea ha un limite di frequenza globale abilitato, il processo decisionale batch richiede un tempo aggiuntivo per essere completato. Di seguito sono riportate alcune approssimazioni del tempo di elaborazione end-to-end per le rispettive dimensioni di segmento, sia con che senza limiti di frequenza per le offerte ammissibili:

Con il limite di frequenza abilitato per le offerte ammissibili:

| Dimensione del segmento | Tempo di elaborazione end-to-end |
|--------------|----------------------------|
| 10 mila profili o meno | 7 minuti |
| 1 milione di profili o meno | 30 minuti |
| 15 milioni di profili o meno | 50 minuti |

Senza limiti di frequenza per le offerte ammissibili:

| Dimensione del segmento | Tempo di elaborazione end-to-end |
|--------------|----------------------------|
| 10 mila profili o meno | 6 minuti |
| 1 milione di profili o meno | 8 minuti |
| 15 milioni di profili o meno | 16 minuti |

## Duplicare una richiesta di lavoro {#duplicate}

È possibile riutilizzare le informazioni di un processo esistente per creare una nuova richiesta.

A questo scopo, fai clic sull’icona duplicata, modifica le informazioni sul processo se necessario, quindi fai clic su **[!UICONTROL Crea]** per creare la nuova richiesta.

![](assets/batch-duplicate.png)
