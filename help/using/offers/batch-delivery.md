---
title: Batch Decisioning
description: Scopri come distribuire le decisioni sulle offerte a tutti i profili in un determinato pubblico Adobe Experience Platform.
badge: label="Legacy" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: 810c05b3-2bae-4368-bf12-3ea8c2f31c01
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 5%

---

# Batch Decisioning {#deliver}

## Introduzione alle decisioni batch {#start}

Journey Optimizer consente di fornire decisioni sulle offerte a tutti i profili in un determinato pubblico Adobe Experience Platform.

A questo scopo, devi creare una richiesta di lavoro in Journey Optimizer che contenga informazioni sul pubblico di destinazione e sulla decisione di offerta da utilizzare. Il contenuto dell’offerta per ogni profilo del pubblico viene quindi inserito in un set di dati Adobe Experience Platform dove è disponibile per flussi di lavoro batch personalizzati.

La consegna in batch può essere eseguita anche utilizzando le API. Per ulteriori informazioni, consulta la [documentazione API Batch Decisioning](api-reference/offer-delivery-api/batch-decisioning-api.md).

## Prerequisiti {#prerequisites}

Prima di configurare una richiesta di processo, assicurati di aver creato:

* **Un set di dati** in Adobe Experience Platform. Questo set di dati verrà utilizzato per memorizzare il risultato della decisione utilizzando lo schema &quot;ODE DecisionEvents&quot;. Ulteriori informazioni sono disponibili nella [documentazione sui set di dati](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=it).

* **Un pubblico** in Adobe Experience Platform. Il pubblico deve essere valutato e quindi aggiornato. Scopri come aggiornare la valutazione dell’iscrizione al pubblico nella [documentazione del servizio di segmentazione](https://www.adobe.com/go/segmentation-overview-en_it)

  >[!NOTE]
  >
  >Un processo batch viene eseguito dallo snapshot del profilo che si verifica una volta al giorno. Le decisioni in batch limitano la frequenza e caricano sempre i profili dallo snapshot più recente. Prima di provare l’API di decisioning in batch, attendi fino a 24 ore dalla creazione di un pubblico.

* **Una decisione** in Adobe Journey Optimizer. [Scopri come creare una decisione](offer-activities/create-offer-activities.md)

<!-- in API doc, remove these info and add ref here-->

## Creare una richiesta di processo

Per creare una nuova richiesta di processo, attieniti alla procedura seguente.

1. Nel menu **[!UICONTROL Offerte]**, apri la scheda **[!UICONTROL Decisioning batch]**, quindi fai clic su **[!UICONTROL Crea richiesta]**.

   ![](assets/batch-create.png)

1. Assegna un nome alla richiesta del processo, quindi seleziona il set di dati in cui devono essere inviati i dati del processo.

1. Seleziona il pubblico Adobe Experience Platform di destinazione.

1. Seleziona uno o più ambiti di decisione delle offerte da utilizzare per distribuire le offerte al pubblico:
   1. Selezionate un posizionamento dall&#39;elenco.
   1. Vengono visualizzate le decisioni disponibili per il posizionamento selezionato. Seleziona la decisione desiderata e fai clic su **[!UICONTROL Aggiungi]**.
   1. Ripeti l’operazione per aggiungere tutti gli ambiti decisionali desiderati.

   ![](assets/batch-decision.png)

1. Per impostazione predefinita, viene restituita un’offerta dell’ambito di decisione per ciascun profilo. È possibile regolare il numero di offerte restituite utilizzando l&#39;opzione **[!UICONTROL Richiedi offerta per profilo]**. Ad esempio, se selezioni 2, verranno visualizzate le 2 offerte migliori per l’ambito decisionale selezionato.

   >[!NOTE]
   >
   >Puoi richiedere fino a 30 offerte per ambito decisionale.

1. Se desideri includere il contenuto dell&#39;offerta nel set di dati, attiva l&#39;opzione **[!UICONTROL Includi contenuto]**. Questa opzione è disabilitata per impostazione predefinita.

1. Fai clic su **[!UICONTROL Crea]** per eseguire la richiesta del processo.

## Monitorare i processi batch

Tutti i processi batch richiesti sono accessibili dalla scheda **[!UICONTROL Decisioning batch]**. Sono inoltre disponibili strumenti di ricerca e filtro che consentono di perfezionare l’elenco.

![](assets/batch-list.png)

### Stati delle richieste di lavoro

Una volta creata una richiesta di processo, il processo batch passa attraverso più stati:

>[!NOTE]
>
>Per essere certi di ottenere le informazioni più recenti sullo stato di una richiesta di lavoro, utilizza il pulsante con i puntini di sospensione accanto al processo per aggiornarlo.

1. **[!UICONTROL In coda]**: la richiesta del processo è stata creata ed è entrata nella coda di elaborazione. È possibile eseguire fino a 5 processi batch alla volta per set di dati. Eventuali altre richieste batch con lo stesso set di dati di output vengono aggiunte alla coda. Un processo in coda viene selezionato per l&#39;elaborazione al termine dell&#39;esecuzione del processo precedente.
1. **[!UICONTROL Elaborazione]**: elaborazione della richiesta di processo in corso
1. **[!UICONTROL Acquisizione]**: la richiesta del processo è stata eseguita, i dati dei risultati vengono acquisiti nel set di dati selezionato,
1. **[!UICONTROL Completato]**: la richiesta del processo è stata eseguita e i dati dei risultati sono ora memorizzati nel set di dati selezionato.

   >[!NOTE]
   >
   >Per accedere al set di dati in cui sono memorizzati i risultati di un processo, fai clic sul nome nell’elenco dei processi.

Se si verifica un errore durante l&#39;esecuzione della richiesta del processo, verrà visualizzato lo stato **[!UICONTROL Errore]**. Prova a duplicare il processo batch per creare una nuova richiesta. [Scopri come duplicare un processo batch](#duplicate)

### Tempo di elaborazione processo batch

Il tempo end-to-end per ogni processo batch è la durata dal momento della creazione del carico di lavoro al momento in cui il risultato della decisione è disponibile nel set di dati di output.

La dimensione del pubblico è il fattore principale che influisce sul tempo di decisione batch end-to-end. Se per l’offerta idonea è abilitato un limite di frequenza globale, il completamento delle decisioni batch richiede un tempo aggiuntivo. Di seguito sono riportate alcune approssimazioni del tempo di elaborazione end-to-end per le rispettive dimensioni di pubblico, con e senza limite di frequenza per le offerte idonee:

Con il limite di frequenza abilitato per le offerte idonee:

| Dimensione del pubblico | Tempo di elaborazione end-to-end |
|--------------|----------------------------|
| 10.000 profili o meno | 7 minuti |
| 1 milione di profili o meno | 30 minuti |
| 15 milioni di profili o meno | 50 minuti |

Senza limite di frequenza per le offerte idonee:

| Dimensione del pubblico | Tempo di elaborazione end-to-end |
|--------------|----------------------------|
| 10.000 profili o meno | 6 minuti |
| 1 milione di profili o meno | 8 minuti |
| 15 milioni di profili o meno | 16 minuti |

## Duplicare una richiesta di lavoro {#duplicate}

È possibile riutilizzare le informazioni di un processo esistente per creare una nuova richiesta.

A tale scopo, fare clic sull&#39;icona del duplicato, modificare le informazioni sul processo, se necessario, quindi fare clic su **[!UICONTROL Crea]** per creare la nuova richiesta.

![](assets/batch-duplicate.png)
