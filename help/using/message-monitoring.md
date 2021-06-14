---
title: Monitorare l’esecuzione dei messaggi
description: Scopri le linee guida per il monitoraggio
feature: Monitoraggio
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 1%

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

<!--For multichannel messages, one row per channel is displayed for each message. STILL VALID? looks like NOT-->

>[!NOTE]
>
>Se un messaggio è stato utilizzato in diversi percorsi, viene visualizzata una riga al percorso per ogni esecuzione.

<!--![](assets/message-execution-multichannel.png)-->

<!--If a message has been used in several journeys, the **[!UICONTROL Source]** column displays **[!UICONTROL Multiple]**.-->

Per impostazione predefinita, i messaggi vengono visualizzati a partire dalla data di esecuzione più recente. Fai clic sull’icona **[!UICONTROL Filters]** per cercare i messaggi in base al canale, alla data di inizio e/o alla data di fine.

![](assets/message-execution-tab-filters.png)

La <!--**[!UICONTROL Quick action]**-->seconda colonna consente di aprire il [messaggio](create-message.md) corrispondente e di accedere al [Live Report](reports/live-report.md) se ti trovi in **[!UICONTROL Live view]** oppure al [Global Report](reports/global-report.md) se ti trovi in **[!UICONTROL Global view]**.

![](assets/message-execution-open-live-report.png)

Per ogni esecuzione del messaggio, vengono visualizzati diversi indicatori:

* **[!UICONTROL Message label]**: Titolo del messaggio definito al momento  [della creazione del messaggio](create-message.md). L’ID di esecuzione, generato automaticamente, viene visualizzato tra parentesi.

   <!--**[!UICONTROL Execution ID]**: Automatically generated identifier.
  **[!UICONTROL Source]**: Name of the journey leveraging that message.-->

* **[!UICONTROL Journey - Version - Action]**: Nome del percorso che sfrutta il messaggio, la versione del percorso e l’etichetta dell’azione che sfrutta il messaggio nel percorso.

* **[!UICONTROL Status]**: Stato di esecuzione del messaggio.  <!--List all the possible statuses? For now only Live status? The user cannot stop or cancel the execution. TBC by Fred-->

* **[!UICONTROL Start date]**: Data e ora in cui il messaggio è stato eseguito dal percorso.

   <!--Targeted: Number of targeted profiles for each message execution. To come?-->

* **[!UICONTROL Excluded]**: Numero di profili che sono stati esclusi dal target iniziale a causa di regole di esclusione.

* **[!UICONTROL Sent]**: Numero di messaggi inviati.

* **[!UICONTROL Delivered]**: Numero di messaggi recapitati correttamente nella cassetta postale (e-mail) o nel dispositivo del destinatario (push) senza generare un messaggio non recapitato o nessun altro errore di consegna.

* **[!UICONTROL Bounces]**: Numero di messaggi che non possono essere recapitati a causa di un errore di consegna. [Ulteriori informazioni sui rimbalzi](suppression-list.md).

* **[!UICONTROL Opens]**: Numero di messaggi aperti.

* **[!UICONTROL Clicks]**: Numero di clic sui collegamenti in un messaggio e-mail.

   >[!NOTE]
   >
   >I clic non esistono per le notifiche push: quando un utente fa clic su una notifica push, apre l&#39;app, che può essere considerata solo come aperta.

* **[!UICONTROL Errors]**: Numero di messaggi che non possono essere inviati a causa di un errore tecnico.

* **[!UICONTROL Spam complaints]**: Numero di messaggi contrassegnati come spam dai destinatari. [Ulteriori informazioni sui reclami](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability).

Facendo clic su ogni collegamento ipertestuale si aprirà la visualizzazione di riepilogo del messaggio corrispondente. [Ulteriori informazioni sui messaggi](create-message.md).
