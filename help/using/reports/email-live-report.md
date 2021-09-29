---
title: Rapporto live delle e-mail
description: Scopri come utilizzare i dati del rapporto live e-mail
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 1ddfbf1a-3cd5-446a-b0fb-76b81b88c1b4
source-git-commit: d814fa98a08d91f1c0744f106c53dd991d544dc2
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 1%

---

# Rapporto live delle e-mail {#email-live-report}

L’e-mail **[!UICONTROL Live report]** esegue il targeting solo di una consegna e-mail specifica.

Dalla scheda **[!UICONTROL Executions]** del menu **[!UICONTROL Messages]** , seleziona **[!UICONTROL Live view]** , quindi dal menu avanzato della consegna selezionata seleziona **[!UICONTROL Live report]**.

![](../assets/live_report.png)

L’e-mail **[!UICONTROL Live report]** è divisa in diversi widget che ne descrivono il successo e gli errori. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questa [sezione](live-report.md#modify-dashboard).

![](../assets/live_report_5.png)

**[!UICONTROL Email performance]** e  **[!UICONTROL Email summary]** i widget descrivono nel dettaglio le informazioni principali relative al messaggio con un grafico e KPI:

* **[!UICONTROL Targeted]**: Numero di profili utente qualificati come profili di destinazione per questa consegna.

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in una consegna.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Spam complaints]**: Numero di messaggi classificati come spam.

* **[!UICONTROL Unsubscriptions]**: Numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Excluded]**: Numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

Il widget **[!UICONTROL Sending Statistics]** descrive il successo della consegna:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

![](../assets/live_report_6.png)

Il grafico e la tabella **[!UICONTROL Error Reasons]** ti consentono di vedere quale errore si è verificato durante la consegna.

I widget **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Hard bounce]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Soft bounce]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignored]**: Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

>[!NOTE]
>
>I profili con stato **[!UICONTROL Suppressed]** o **[!UICONTROL Not allowed]** sono esclusi durante il processo di invio del messaggio. Pertanto, mentre i **rapporti sul Percorso** mostreranno questi profili come spostati attraverso il percorso ([Leggi segmento](../building-journeys/read-segment.md) e [Messaggio](../building-journeys/journeys-message.md)), i **Rapporti e-mail** non li includeranno nelle metriche **[!UICONTROL Sent]** in quanto vengono filtrati prima dell’invio dell’e-mail.
>
>Ulteriori informazioni sull&#39; [Elenco di soppressione](../suppression-list.md) e sull&#39; [Elenco Consentiti](../allow-list.md). Per scoprire il motivo di tutti i casi di esclusione, puoi utilizzare il [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
