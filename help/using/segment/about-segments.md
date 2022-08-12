---
title: Informazioni sui segmenti di Adobe Experience Platform
description: Scopri come configurare un segmento Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 2%

---

# Guida introduttiva ai segmenti Adobe Experience Platform {#about-segments}

[!DNL Journey Optimizer]  consente di creare segmenti Adobe Experience Platform utilizzando i dati del profilo cliente in tempo reale direttamente dal **[!UICONTROL Segments]** e sfruttali nei tuoi percorsi.

I segmenti possono essere creati anche dal servizio Segmentazione stesso. Ulteriori informazioni nel [Documentazione del servizio di segmentazione Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

Puoi sfruttare i segmenti nei percorsi in diversi modi:

* Utilizza un **Leggi segmento** attività di orchestrazione per fare entrare nel percorso tutti gli individui appartenenti al segmento specificato. I messaggi inclusi nel percorso vengono inviati agli utenti appartenenti al segmento. Supponiamo che tu abbia un segmento &quot;cliente argento&quot;. Con questa attività, puoi fare in modo che tutti i clienti argento entrino in un percorso e inviino loro una serie di messaggi personalizzati.

   Per ulteriori informazioni su come utilizzare il **[!UICONTROL Read segment]** attività, fai riferimento a [questa sezione](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilizza la **Qualificazione di un segmento** attività dell’evento per consentire a singoli utenti di entrare o proseguire in un percorso in base alle entrate e alle uscite dei segmenti Adobe Experience Platform. Ad esempio, puoi fare in modo che tutti i nuovi clienti argento entrino in un percorso e inviino loro messaggi. Per ulteriori informazioni su come utilizzare questa attività, consulta [questa sezione](../building-journeys/segment-qualification-events.md).

* Crea **condizioni complesse** nei percorsi utilizzando l’editor di espressioni semplice o avanzato. Ulteriori informazioni in [questa sezione](../building-journeys/condition-activity.md#using-a-segment).

## Metodo di valutazione in Adobe Journey Optimizer {#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer, i tipi di pubblico vengono generati dalle definizioni dei segmenti utilizzando uno dei seguenti metodi di valutazione:

* Segmentazione in streaming : l’elenco del pubblico per il segmento viene mantenuto aggiornato in tempo reale, mentre i nuovi dati scorrono nel sistema.
* Segmentazione in batch: l’elenco del pubblico per il segmento viene aggiornato ogni ora, in base ai dati arrivati nell’ora precedente.

La determinazione tra segmentazione batch e segmentazione in streaming viene effettuata dal sistema per ogni definizione di segmento, in base alla complessità e al costo della valutazione della regola del segmento.

Puoi visualizzare il metodo di valutazione per ogni segmento nel **[!UICONTROL Evaluation method]** della colonna dell’elenco dei segmenti.

Dopo aver definito per la prima volta un segmento, i profili vengono aggiunti al pubblico quando si qualificano.

Il backfill del pubblico dai dati precedenti può richiedere fino a 24 ore. Dopo che il pubblico è stato riempito di nuovo, il pubblico viene costantemente aggiornato ed è sempre pronto per il targeting.
