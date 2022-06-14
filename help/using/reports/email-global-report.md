---
title: Rapporto globale delle e-mail
description: Scopri come utilizzare i dati del report globale e-mail
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 2bead395-082a-4fea-ad10-b2b2c5f484e9
source-git-commit: 0ca491315e214e3c12bec11a93da1a2b98b493b6
workflow-type: tm+mt
source-wordcount: '734'
ht-degree: 0%

---

# Rapporto globale delle e-mail {#email-global-report}

L’e-mail **[!UICONTROL Global report]** esegue solo il targeting di una consegna e-mail specifica.

Da **[!UICONTROL Executions]** della scheda **[!UICONTROL Messages]** menu, seleziona **[!UICONTROL Global view]** dal menu avanzato della consegna selezionata, seleziona **[!UICONTROL Global report]**.

![](assets/global_report_3.png)

L’e-mail **[!UICONTROL Global report]** è suddiviso in diversi widget che descrivono in dettaglio il successo e gli errori della consegna. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni su questo consulta [sezione](global-report.md#modify-dashboard).

![](assets/global_report_4.png)

**[!UICONTROL Email performance]** fornisce dettagli sulle informazioni principali relative al messaggio con KPI:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivery Rate]**: Percentuale di messaggi inviati correttamente.

* **[!UICONTROL Bounce Rate]**: Percentuale di e-mail rimbalzate rispetto alle e-mail inviate.

* **[!UICONTROL Error Rate]**: Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle e-mail inviate.

* **[!UICONTROL Open Rate]**: Percentuale di messaggi aperti.

* **[!UICONTROL Click Rate]**: Percentuale di clic in una consegna.

* **[!UICONTROL Spam Complaint Rate]**: Percentuale di e-mail contrassegnate come spam dai destinatari rispetto ai messaggi consegnati. Per ulteriori informazioni sui reclami, consulta [Guida alle best practice per il recapito messaggi](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/metrics-for-deliverability/complaints.html#metrics-for-deliverability){target=&quot;_blank&quot;}.

* **[!UICONTROL Unsubscribe Rate]**: Percentuale di annullamenti univoci delle sottoscrizioni rispetto al numero di messaggi inviati. Questo indicatore non si basa sul numero di clic sul collegamento di annullamento dell’abbonamento, ma si basa sul numero di annullamenti di abbonamenti avviati dai destinatari. Ulteriori informazioni sugli annullamenti di abbonamenti in questo [page](../messages/consent.md).

La **[!UICONTROL Email - Tracking statistics]** contiene i dati disponibili per l’attività del destinatario per la consegna:

* **[!UICONTROL Opens]**: Numero di volte in cui la consegna è stata aperta in una consegna.

* **[!UICONTROL Unique Opens]**: Percentuale di consegne aperte.

* **[!UICONTROL Open Rate]**: Numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Unique Clicks]**:numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Click through rate]**: Percentuale di utenti che hanno interagito con il percorso.

La **[!UICONTROL Sending Statistics]** il grafico descrive il successo della consegna:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

![](assets/global_report_5.png)

La **[!UICONTROL Bounce Reasons]** e **[!UICONTROL Bounce categories]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Hard bounce]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Soft bounce]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignored]**: Numero totale di temporanei, ad esempio fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Per ulteriori informazioni sui messaggi non recapitati, consulta [Elenco di eliminazione](../reports/suppression-list.md) pagina.

La **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

![](assets/global_report_6.png)

La **[!UICONTROL Email - Top recipient domain]** visualizza i dettagli del grafico e della tabella relativi ai domini più utilizzati dai destinatari per aprire l’e-mail.

La **[!UICONTROL Email - Top Url]** grafico e tabelle che specificano gli URL della consegna più visitati.

La **[!UICONTROL Open vs Click]** identifica l’interazione dei destinatari con la consegna:

* **[!UICONTROL Unique Clicks]**:numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Unique Opens]**: Numero di destinatari che hanno aperto la consegna.

![](assets/global_report_20.png)

>[!NOTE]
>
>I widget e le metriche Offerte sono disponibili solo se una decisione è stata inserita in un’e-mail. Per ulteriori informazioni sulla gestione delle decisioni, consulta questo [page](../offers/get-started/starting-offer-decisioning.md).

La **[!UICONTROL Offers statistic]** e **[!UICONTROL Offers statistics]** i widget nel tempo misurano il successo e l’impatto dell’offerta sul pubblico di destinazione. Vengono descritte in dettaglio le informazioni principali relative al messaggio con i KPI:

* **[!UICONTROL Offer sent]**: Numero totale di invii per l’offerta.

* **[!UICONTROL Offer impression]**: Numero di volte in cui l’offerta è stata aperta in una consegna.

* **[!UICONTROL Offer clicks]**: Numero di volte in cui un’offerta è stata selezionata in una consegna.

La **[!UICONTROL Offers detailed statistic]** La tabella contiene i dati disponibili per l’attività del destinatario con l’offerta:

* **[!UICONTROL Placement name]**: Nome del posizionamento utilizzato per visualizzare l’offerta. Per ulteriori informazioni sul posizionamento, consulta questo [page](../offers/offer-library/creating-placements.md).

* **[!UICONTROL Offer name]**: Nome dell’offerta aggiunta nella consegna. Per ulteriori informazioni sul posizionamento, consulta questo [page](../offers/offer-library/creating-personalized-offers.md).

* **[!UICONTROL Offer sent]**: Numero totale di invii per l’offerta.

* **[!UICONTROL Offer impression rate]**: Percentuale di offerte aperte rispetto al numero di offerte inviate.

* **[!UICONTROL Offer click rate]**: Percentuale di utenti che hanno interagito con l’offerta.

>[!NOTE]
>
>I profili con **[!UICONTROL Suppressed]** o **[!UICONTROL Not allowed]** lo stato viene escluso durante il processo di invio del messaggio. Pertanto, mentre **Rapporti sui percorsi** mostrerà questi profili come spostati nel percorso ([Leggi segmento](../building-journeys/read-segment.md) e [Messaggio](../building-journeys/journeys-message.md) attività), **Rapporti e-mail** non li includerà nella **[!UICONTROL Sent]** le metriche vengono filtrate prima dell’invio dell’e-mail.
>
>Per saperne di più sul [Elenco di eliminazione](suppression-list.md) e [Elenco Consentiti](../configuration/allow-list.md). Per scoprire il motivo di tutti i casi di esclusione, puoi utilizzare il [Servizio query Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.
