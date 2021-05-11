---
title: Monitorare l’esecuzione dei messaggi
description: Scopri le linee guida per il monitoraggio
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# Monitoraggio dei messaggi {#monitor-message-execution}

![](assets/do-not-localize/badge.png)

Per garantire che i messaggi siano eseguiti, inviati e consegnati correttamente, [!DNL Journey Optimizer] offre funzionalità per monitorare i messaggi attualmente pubblicati e attivati. Puoi vedere in tempo reale le prestazioni dei messaggi tra percorsi <!--and APIs--> dall&#39;elenco **[!UICONTROL Executions]**.

Per accedere a questo elenco, dalla home page di **[!DNL Journey Optimizer]** selezionare **[!UICONTROL Messages]** e fare clic sulla scheda **[!UICONTROL Executions]**.

Questa scheda fornisce due visualizzazioni: **[!UICONTROL Live view]** e **[!UICONTROL Global view]**.

* La scheda **[!UICONTROL Live view]** fornisce una panoramica in tempo reale di tutti i messaggi eseguiti **attivati da uno o più [percorsi](building-journeys/journey.md)** solo nelle ultime 24 ore **.**

   ![](assets/message-execution-tab-live.png)

   Questo elenco si aggiorna automaticamente ogni sessanta secondi. Se non si è verificata alcuna esecuzione nelle ultime 24 ore per un messaggio specifico, tutte le colonne visualizzeranno valori nulli (0) per quel messaggio.

* La scheda **[!UICONTROL Global view]** fornisce una **panoramica di tutti i messaggi eseguiti** attivati da uno o più [percorsi](building-journeys/journey.md) **a partire dalla data di inizio del messaggio**.

   ![](assets/message-execution-tab-global.png)

   Questa lista si aggiorna automaticamente ogni novanta minuti. I dati sono aggregati nel tempo a partire dalla data di inizio di ciascun messaggio.

Se un messaggio viene pubblicato ma non è ancora attivato da un percorso, non viene elencato in nessuna delle schede. Sono elencati solo i seguenti elementi:
* Messaggi attivati, ma non ancora avviati (in sospeso).
* Messaggi attivati e attualmente in esecuzione (in corso).

Per i messaggi multicanale, viene visualizzata una riga per canale per ogni messaggio.

![](assets/message-execution-multichannel.png)

Se un messaggio è stato utilizzato in diversi percorsi, la colonna **[!UICONTROL Source]** visualizza **[!UICONTROL Multiple]**.

Per impostazione predefinita, i messaggi vengono visualizzati a partire dalla data di esecuzione più recente. Fai clic sull’icona **[!UICONTROL Filters]** per cercare i messaggi in base al canale, alla data di inizio e/o alla data di fine.

![](assets/message-execution-tab-filters.png)

La <!--**[!UICONTROL Quick action]**-->seconda colonna consente di aprire il [messaggio](create-message.md) corrispondente e di accedere al [Live Report](reports/live-report.md) se ti trovi in **[!UICONTROL Live view]** oppure al [Global Report](reports/global-report.md) se ti trovi in **[!UICONTROL Global view]**.

![](assets/message-execution-open-live-report.png)

Per ogni esecuzione del messaggio, vengono visualizzati diversi indicatori:

* **[!UICONTROL Message label]**: Titolo del messaggio definito al momento  [della creazione del messaggio](create-message.md).
* **[!UICONTROL Execution ID]**: Identificatore generato automaticamente.
* **[!UICONTROL Source]**: Nome del percorso che sfrutta il messaggio.
* **[!UICONTROL Start date]**: Data e ora in cui il messaggio è stato eseguito dal percorso.
* **[!UICONTROL Excluded]**: Numero di profili che sono stati esclusi dal target iniziale a causa di regole di esclusione.
* **[!UICONTROL Sent]**: Numero di messaggi inviati.
* **[!UICONTROL Delivered]**: Numero di messaggi recapitati correttamente nella cassetta postale (e-mail) o nel dispositivo del destinatario (push) senza generare un messaggio non recapitato o nessun altro errore di consegna.
* **[!UICONTROL Bounces]**: Numero di messaggi che non possono essere recapitati a causa di un errore di consegna. [Ulteriori informazioni sui mancati recapiti](suppression-lists.md#delivery-failures).
* **[!UICONTROL Opens]**: Numero di messaggi aperti.
* **[!UICONTROL Clicks]**: Numero di clic sui collegamenti in un messaggio e-mail.

   >[!NOTE]
   >
   >I clic non esistono per le notifiche push: quando un utente fa clic su una notifica push, apre l&#39;app, che può essere considerata solo come aperta.

* **[!UICONTROL Errors]**: Numero di messaggi che non possono essere inviati a causa di un errore tecnico.

Facendo clic su ogni collegamento ipertestuale si aprirà la visualizzazione di riepilogo del messaggio corrispondente. [Ulteriori informazioni sui messaggi](create-message.md).
