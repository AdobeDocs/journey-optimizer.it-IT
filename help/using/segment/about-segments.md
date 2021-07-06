---
title: Informazioni sui segmenti Adobe Experience Platform
description: Scopri come configurare un segmento Adobe Experience Platform
feature: Percorsi
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: b07970ff11f1ba7c4e6db30dc2eca1252a579ca4
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 2%

---

# Introduzione ai segmenti {#about-segments}

[!DNL Journey Optimizer] consente di creare segmenti Adobe Experience Platform utilizzando i dati Profilo cliente in tempo reale direttamente dal  **[!UICONTROL Segments]** menu e di sfruttarli nei percorsi.

I segmenti possono essere creati anche dal servizio Segmentazione stesso. Ulteriori informazioni sono disponibili nella [documentazione del servizio di segmentazione Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html){target=&quot;_blank&quot;}.

Puoi sfruttare i segmenti nei percorsi in diversi modi:

* Utilizza un&#39;attività di orchestrazione **Leggi segmento** per fare in modo che tutti gli individui appartenenti al segmento specificato entrino nel percorso. I messaggi inclusi nel percorso vengono inviati agli utenti appartenenti al segmento. Supponiamo che tu abbia un segmento &quot;cliente argento&quot;. Con questa attività, puoi fare in modo che tutti i clienti argento entrino in un percorso e inviino loro una serie di messaggi personalizzati.

   Per ulteriori informazioni su come utilizzare l&#39;attività **[!UICONTROL Read segment]**, consulta [questa sezione](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilizza l’attività dell’evento **Qualificazione del segmento** per consentire ai singoli utenti di entrare o proseguire in un percorso in base alle entrate e alle uscite dei segmenti Adobe Experience Platform. Ad esempio, puoi fare in modo che tutti i nuovi clienti argento entrino in un percorso e inviino loro messaggi. Per ulteriori informazioni su come utilizzare questa attività, consulta [questa sezione](../building-journeys/segment-qualification-events.md).

* Crea **condizioni complesse** nei tuoi percorsi utilizzando l’editor di espressioni semplice o avanzato. [Ulteriori informazioni](../building-journeys/condition-activity.md#using-a-segment).

## Metodo di valutazione in Adobe Journey Optimizer {#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer, i tipi di pubblico vengono generati dalle definizioni dei segmenti utilizzando uno dei seguenti metodi di valutazione:

* Segmentazione in streaming: l’elenco dei tipi di pubblico per il segmento viene tenuto aggiornato in tempo reale mentre i nuovi dati arrivano nel sistema.
* Segmentazione in batch: l’elenco del pubblico per il segmento viene aggiornato ogni ora, in base ai dati arrivati nell’ora precedente.

La determinazione tra segmentazione batch e segmentazione in streaming viene effettuata dal sistema per ogni definizione di segmento, in base alla complessità e al costo della valutazione della regola del segmento.

Puoi visualizzare il metodo di valutazione per ciascun segmento nella colonna **[!UICONTROL Evaluation method]** dell’elenco dei segmenti.

Dopo aver definito per la prima volta un segmento, i profili vengono aggiunti al pubblico quando si qualificano.

Il backfill del pubblico dai dati precedenti può richiedere fino a 24 ore. Dopo che il pubblico è stato riempito di nuovo, il pubblico viene costantemente aggiornato ed è sempre pronto per il targeting.
