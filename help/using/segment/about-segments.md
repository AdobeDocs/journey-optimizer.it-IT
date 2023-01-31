---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sui segmenti di Adobe Experience Platform
description: Scopri come configurare un segmento Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 78675ca22d8ee9a93d9af128d5708c305523da78
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Guida introduttiva ai segmenti Adobe Experience Platform {#about-segments}

[!DNL Journey Optimizer]  consente di creare segmenti Adobe Experience Platform utilizzando i dati del profilo cliente in tempo reale direttamente dal **[!UICONTROL Segmenti]** e utilizzali nei tuoi percorsi o campagne.

Inoltre, i segmenti possono essere creati anche dal servizio Segmentazione stesso. Ulteriori informazioni nel [Documentazione del servizio di segmentazione Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Utilizzare i segmenti in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puoi sfruttare i segmenti in **[!DNL Journey Optimizer]** in diversi modi:

* Scegli un segmento come **pubblico per una campagna**, in cui il messaggio viene inviato a tutti gli utenti appartenenti al segmento selezionato. [Scopri come definire il pubblico di una campagna](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilizza un **Leggi segmento** attività di orchestrazione in un percorso per consentire a tutti gli utenti del segmento di entrare nel percorso e ricevere i messaggi inclusi nel percorso.

   Supponiamo che tu abbia un segmento &quot;cliente argento&quot;. Con questa attività, puoi fare in modo che tutti i clienti argento entrino in un percorso e inviino loro una serie di messaggi personalizzati. [Scopri come configurare un’attività Leggi segmento](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilizza la **Qualificazione di un segmento** attività evento in un percorso per consentire a singoli utenti di entrare o proseguire nel percorso in base alle entrate e alle uscite dei segmenti Adobe Experience Platform.

   Ad esempio, puoi fare in modo che tutti i nuovi clienti argento entrino in un percorso e inviino loro messaggi. Per ulteriori informazioni su come utilizzare questa attività, consulta [Scopri come configurare un’attività di qualificazione dei segmenti](../building-journeys/segment-qualification-events.md).

* Utilizza la **Condizione** attività in un percorso per creare condizioni basate sull’appartenenza al segmento. [Scopri come utilizzare i segmenti nelle condizioni](../building-journeys/condition-activity.md#using-a-segment).

## Metodi di valutazione del pubblico{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer, i tipi di pubblico vengono generati dalle definizioni dei segmenti utilizzando uno dei due metodi di valutazione seguenti:

* **Segmentazione streaming**: L’elenco del pubblico per il segmento viene mantenuto aggiornato in tempo reale man mano che i nuovi dati scorrono nel sistema.

   La segmentazione in streaming è un processo continuo di selezione dei dati che aggiorna i segmenti in risposta all’attività dell’utente. Una volta generato e salvato un segmento, la definizione del segmento viene applicata ai dati in arrivo in Journey Optimizer. Questo significa che i singoli utenti vengono aggiunti o rimossi dal segmento quando i dati del loro profilo cambiano, garantendo che il pubblico di destinazione sia sempre rilevante.

* **Segmentazione in batch**: L’elenco del pubblico per il segmento viene valutato ogni 24 ore.

   La segmentazione in batch è un’alternativa alla segmentazione in streaming che elabora tutti i dati di profilo contemporaneamente attraverso le definizioni dei segmenti. Crea un’istantanea del pubblico che può essere salvata ed esportata per l’utilizzo. Tuttavia, a differenza della segmentazione in streaming, la segmentazione in batch non aggiorna continuamente l’elenco dei tipi di pubblico in tempo reale, e i nuovi dati che arrivano dopo il processo batch non verranno riportati nel segmento fino al successivo processo batch.&quot;

La determinazione tra segmentazione batch e segmentazione in streaming viene effettuata dal sistema per ogni definizione di segmento, in base alla complessità e al costo della valutazione della regola del segmento. Puoi visualizzare il metodo di valutazione per ogni segmento nel **[!UICONTROL Metodo di valutazione]** della colonna dell’elenco dei segmenti.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Se la **[!UICONTROL Metodo di valutazione]** la colonna non viene visualizzata, è necessario aggiungerla utilizzando il pulsante di configurazione in alto a destra dell’elenco.

Dopo aver definito per la prima volta un segmento, i profili vengono aggiunti al pubblico quando si qualificano.

Il backfill del pubblico dai dati precedenti può richiedere fino a 24 ore. Dopo che il pubblico è stato riempito di nuovo, il pubblico viene costantemente aggiornato ed è sempre pronto per il targeting.
