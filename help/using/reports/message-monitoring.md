---
title: Monitorare l’esecuzione dei messaggi
description: Scopri le linee guida per il monitoraggio
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 950f8186-07f6-4cc1-936c-d0984fb0f988
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '617'
ht-degree: 1%

---

# Monitoraggio dei messaggi {#monitor-message-execution}

Per verificare che i messaggi siano correttamente eseguiti, inviati e consegnati, [!DNL Journey Optimizer] offre funzionalità per monitorare i messaggi attualmente pubblicati e attivati. Puoi vedere le prestazioni dei messaggi tra percorsi diversi <!--and APIs--> in tempo reale dal **[!UICONTROL Executions]** elenco.

➡️ [Scopri questa funzione nel video](#video)

Per accedere a questo elenco, dal **[!DNL Journey Optimizer]** home page, seleziona **[!UICONTROL Messages]**, quindi fai clic su **[!UICONTROL Executions]** scheda .

Questa scheda fornisce due visualizzazioni: **[!UICONTROL Live view]** e **[!UICONTROL Global view]**.

* La **[!UICONTROL Live view]** fornisce una scheda **panoramica in tempo reale di tutti i messaggi eseguiti** attivato da uno o più [percorsi](../building-journeys/journey.md) **solo nelle ultime 24 ore**.

   ![](assets/message-execution-tab-live.png)

   Questo elenco si aggiorna automaticamente ogni sessanta secondi. Se non si è verificata alcuna esecuzione nelle ultime 24 ore per un messaggio specifico, tutte le colonne visualizzeranno valori nulli (0) per quel messaggio.

* La **[!UICONTROL Global view]** La scheda fornisce un **panoramica di tutti i messaggi eseguiti** attivato da uno o più [percorsi](../building-journeys/journey.md) **dalla data di inizio del messaggio**.

   ![](assets/message-execution-tab-global.png)

   Questa lista si aggiorna automaticamente ogni novanta minuti. I dati sono aggregati nel tempo a partire dalla data di inizio di ciascun messaggio.

Se un messaggio viene pubblicato ma non è ancora attivato da un percorso, non viene elencato in nessuna delle schede. Sono elencati solo i seguenti elementi:
* Messaggi attivati, ma non ancora avviati (in sospeso).
* Messaggi attivati e attualmente in esecuzione (in corso).

>[!NOTE]
>
>Se un messaggio è stato utilizzato in diversi percorsi, viene visualizzata una riga al percorso per ogni esecuzione.

Per impostazione predefinita, i messaggi vengono visualizzati a partire dalla data di esecuzione più recente. Fai clic sul pulsante **[!UICONTROL Filters]** per cercare i messaggi in base al canale, alla data di inizio e/o alla data di fine. Puoi anche scegliere di escludere gli eventi di test dal tuo **Elenco esecuzioni**.

![](assets/message-execution-tab-filters.png)

La <!--**[!UICONTROL Quick action]**-->la seconda colonna consente di aprire la corrispondente [message](../messages/get-started-content.md) e di accedere al [Report live](../reports/live-report.md) se sei nel **[!UICONTROL Live view]** o [Report globale](../reports/global-report.md) se sei nel **[!UICONTROL Global view]**.

![](assets/message-execution-open-live-report.png)

Per ogni esecuzione del messaggio, vengono visualizzati diversi indicatori:

* **[!UICONTROL Message label]**: Titolo del messaggio definito [creazione del messaggio](../messages/get-started-content.md). L’ID di esecuzione, generato automaticamente, viene visualizzato tra parentesi.

   <!--**[!UICONTROL Execution ID]**: Automatically generated identifier.
  **[!UICONTROL Source]**: Name of the journey leveraging that message.-->

* **[!UICONTROL Journey - Version - Action]**: Nome del percorso che sfrutta il messaggio, la versione del percorso e l’etichetta dell’azione che sfrutta il messaggio nel percorso.

* **[!UICONTROL Status]**: Stato di esecuzione del messaggio.

* **[!UICONTROL Start date]**: Data e ora in cui il messaggio è stato eseguito dal percorso.

* **[!UICONTROL Targeted]**: Numero di profili target per ogni esecuzione dei messaggi.

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

* **[!UICONTROL Spam complaints]**: Numero di messaggi contrassegnati come spam dai destinatari. Ulteriori informazioni sui reclami nel [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

È possibile scegliere le colonne da visualizzare nella tabella. A tale scopo, fai clic sul pulsante **[!UICONTROL Customize table]** nella parte superiore dello schermo e seleziona le colonne da visualizzare.

![](assets/message-execution-customize-table.png)

In **Vista globale** Solo, puoi scegliere se visualizzare i dati come numeri, percentuali o entrambi. Fai clic sul pulsante **Formato dati** elenco a discesa per scegliere tra le tre opzioni.

![](assets/message-execution-data-format.png)

Facendo clic su ogni collegamento ipertestuale si aprirà la visualizzazione di riepilogo del messaggio corrispondente. [Ulteriori informazioni sui messaggi](../messages/get-started-content.md).

## Video introduttivo {#video}

Scopri di più sui rapporti live e globali, come accedere e analizzare il Percorso e i rapporti specifici per il messaggio e come modificare le dashboard dei rapporti.

>[!VIDEO](https://video.tv.adobe.com/v/334108?quality=12)
