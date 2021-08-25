---
title: Rapporto globale delle e-mail
description: Scopri come utilizzare i dati del report globale e-mail
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: c54e4443c0a8b6c2e427fa007adf5d800b2ba3b5
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 1%

---

# Rapporto globale delle e-mail {#email-global-report}

L’e-mail **[!UICONTROL Global report]** esegue il targeting solo di una consegna e-mail specifica.

Dalla scheda **[!UICONTROL Executions]** del menu **[!UICONTROL Messages]** , seleziona **[!UICONTROL Global view]** , quindi dal menu avanzato della consegna selezionata seleziona **[!UICONTROL Global report]**.

![](../assets/global_report_3.png)

L’e-mail **[!UICONTROL Global report]** è divisa in diversi widget che ne descrivono il successo e gli errori. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questa [sezione](global-report.md#modify-dashboard).

![](../assets/global_report_4.png)

**[!UICONTROL Email performance]** fornisce dettagli sulle informazioni principali relative al messaggio con KPI:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivery Rate]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Bounce Rate]**: Percentuale di e-mail rimbalzate rispetto alle e-mail inviate.

* **[!UICONTROL Error Rate]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle e-mail inviate.

* **[!UICONTROL Open Rate]**: Percentuale di messaggi aperti.

* **[!UICONTROL Click Rate]**: Percentuale di clic in una consegna.

* **[!UICONTROL Spam Complaint Rate]**: Percentuale di e-mail contrassegnate come spam dai destinatari rispetto ai messaggi consegnati. Per ulteriori informazioni sui reclami, consulta la [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

* **[!UICONTROL Unsubscribe Rate]**: Percentuale di annullamenti univoci delle sottoscrizioni rispetto al numero di messaggi inviati. Questo indicatore non si basa sul numero di clic sul collegamento di annullamento dell’abbonamento, ma si basa sul numero di annullamenti di abbonamenti avviati dai destinatari. Ulteriori informazioni sugli annullamenti di abbonamenti in questa [pagina](../consent.md).

Il **[!UICONTROL Email - Tracking statistics]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Opens]**: Numero di volte in cui la consegna è stata aperta in una consegna.

* **[!UICONTROL Unique Opens]**: Percentuale di consegne aperte.

* **[!UICONTROL Open Rate]**: Numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Unique Clicks]**:numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Click through rate]**: Percentuale di utenti che hanno interagito con il percorso.

Il grafico **[!UICONTROL Sending Statistics]** descrive il successo della consegna:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

![](../assets/global_report_5.png)

I widget **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Hard bounce]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Soft bounce]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignored]**: Numero totale di temporanei, ad esempio fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Per ulteriori informazioni sui messaggi non recapitati, consulta la pagina [Elenco di eliminazione](../suppression-list.md) .

Il grafico e la tabella **[!UICONTROL Error Reasons]** ti consentono di vedere quale errore si è verificato durante la consegna.

![](../assets/global_report_6.png)

Il grafico **[!UICONTROL Email - Top recipient domain]** e la tabella mostrano i dettagli dei domini più utilizzati dai destinatari per aprire l’e-mail.

Il grafico e la tabella **[!UICONTROL Email - Top Url]** mostrano gli URL della consegna più visitati.

L’ **[!UICONTROL Open vs Click]** identifica l’interazione dei destinatari con la consegna:

* **[!UICONTROL Unique Clicks]**:numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Unique Opens]**: Numero di destinatari che hanno aperto la consegna.

>[!NOTE]
>
>I profili con stato **[!UICONTROL Suppressed]** o **[!UICONTROL Not allowed]** sono esclusi durante il processo di invio del messaggio. Pertanto, mentre i **rapporti sul Percorso** mostreranno questi profili come spostati attraverso il percorso ([Leggi segmento](../building-journeys/read-segment.md) e [Messaggio](../building-journeys/journeys-message.md)), i **Rapporti e-mail** non li includeranno nelle metriche **[!UICONTROL Sent]** in quanto vengono filtrati prima dell’invio dell’e-mail.
>
>Ulteriori informazioni sull&#39; [Elenco di soppressione](../suppression-list.md) e sull&#39; [Elenco Consentiti](../allow-list.md). Per scoprire il motivo di tutti i casi di esclusione, puoi utilizzare il [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html).