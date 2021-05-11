---
title: Informazioni sui segmenti Adobe Experience Platform
description: Scopri come configurare un segmento Adobe Experience Platform
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Informazioni sui segmenti Adobe Experience Platform {#about-segments}

![](../assets/do-not-localize/badge.png)

Journey Optimizer ti consente di creare segmenti Adobe Experience Platform utilizzando i dati Profilo cliente in tempo reale direttamente dal menu **[!UICONTROL Segments]** e di sfruttarli nei tuoi percorsi.

I segmenti possono essere creati anche dal servizio Segmentazione stesso. Ulteriori informazioni sono disponibili nella [documentazione del servizio di segmentazione Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

Puoi sfruttare i segmenti nei percorsi in diversi modi:

* Utilizza un&#39;attività di orchestrazione **Leggi segmento** per fare in modo che tutti gli individui appartenenti al segmento specificato entrino nel percorso. I messaggi inclusi nel percorso vengono inviati agli utenti appartenenti al segmento. Supponiamo che tu abbia un segmento &quot;cliente argento&quot;. Con questa attività, puoi fare in modo che tutti i clienti argento entrino in un percorso e inviino loro una serie di messaggi personalizzati.

   Per ulteriori informazioni su come utilizzare l&#39;attività **[!UICONTROL Read segment]**, consulta [questa sezione](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilizza l’attività dell’evento **Qualificazione del segmento** per consentire ai singoli utenti di entrare o proseguire in un percorso in base alle entrate e alle uscite dei segmenti Adobe Experience Platform. Ad esempio, puoi fare in modo che tutti i nuovi clienti argento entrino in un percorso e inviino loro messaggi. Per ulteriori informazioni su come utilizzare questa attività, consulta [questa sezione](../building-journeys/segment-qualification-events.md).

* Crea **condizioni complesse** nei tuoi percorsi utilizzando l’editor di espressioni semplice o avanzato. Ulteriori informazioni in [questa sezione](../building-journeys/condition-activity.md#using-a-segment).
