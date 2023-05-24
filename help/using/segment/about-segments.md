---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sui segmenti di Adobe Experience Platform
description: Scopri come configurare un segmento di Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 6c255d66fb89ba756add062d8a4315dd622fd8e7
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 8%

---

# Introduzione ai segmenti di Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Segmento"
>abstract="Sfruttando i dati del servizio Real-Time Customer Profile, Adobe Experience Platform consente di creare facilmente segmenti mirati che acquisiscono i comportamenti e le preferenze unici dei tuoi clienti."

[!DNL Journey Optimizer]  consente di creare segmenti di Adobe Experience Platform utilizzando i dati Real-Time Customer Profile direttamente dal **[!UICONTROL Segmenti]** e utilizzarli nei percorsi o nelle campagne.

Inoltre, è possibile creare segmenti anche dal servizio di segmentazione stesso. Per ulteriori informazioni, consulta [Documentazione del servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

## Utilizzare i segmenti in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puoi sfruttare i segmenti in **[!DNL Journey Optimizer]** in modi diversi:

* Scegli un segmento come **pubblico per una campagna**: il messaggio viene inviato a tutte le persone appartenenti al segmento selezionato. [Scopri come definire il pubblico di una campagna](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilizza un **Leggi segmento** attività di orchestrazione in un percorso per fare in modo che tutti i singoli utenti del segmento entrino nel percorso e ricevano i messaggi inclusi nel percorso.

   Supponiamo che tu abbia un segmento &quot;cliente silver&quot;. Con questa attività, puoi fare in modo che tutti i clienti silver entrino in un percorso e inviino loro una serie di messaggi personalizzati. [Scopri come configurare un’attività Leggi segmento](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilizza il **Qualificazione del segmento** attività evento in un percorso per consentire ai singoli utenti di entrare o proseguire nel percorso in base alle entrate e alle uscite del segmento Adobe Experience Platform.

   Ad esempio, puoi fare in modo che tutti i nuovi clienti silver entrino in un percorso e inviino loro messaggi. Per ulteriori informazioni su come utilizzare questa attività, consulta [Scopri come configurare un’attività di qualificazione dei segmenti](../building-journeys/segment-qualification-events.md).

* Utilizza il **Condizione** attività in un percorso per creare condizioni basate sull’iscrizione al segmento. [Scopri come utilizzare i segmenti nelle condizioni](../building-journeys/condition-activity.md#using-a-segment).

## Metodi di valutazione del pubblico{#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer, i tipi di pubblico vengono generati dalle definizioni dei segmenti utilizzando uno dei due metodi di valutazione seguenti:

* **Segmentazione in streaming**: l’elenco del pubblico per il segmento viene tenuto aggiornato in tempo reale man mano che nuovi dati fluiscono nel sistema.

   La segmentazione in streaming è un processo continuo di selezione dei dati che aggiorna i segmenti in risposta all’attività dell’utente. Una volta creato e salvato un segmento, la definizione del segmento viene applicata ai dati in arrivo in Journey Optimizer. Ciò significa che gli individui vengono aggiunti o rimossi dal segmento con la modifica dei dati del loro profilo, garantendo che il pubblico di destinazione sia sempre rilevante.

* **Segmentazione batch**: l’elenco dei tipi di pubblico per il segmento viene valutato ogni 24 ore.

   La segmentazione in batch è un’alternativa alla segmentazione in streaming che elabora tutti i dati di profilo contemporaneamente tramite le definizioni dei segmenti. In questo modo viene creata un’istantanea del pubblico che può essere salvato ed esportato per l’utilizzo. Tuttavia, a differenza della segmentazione in streaming, la segmentazione in batch non aggiorna continuamente l’elenco del pubblico in tempo reale e i nuovi dati che arrivano dopo il processo batch non verranno riflessi nel segmento fino al successivo processo batch.&quot;

La determinazione tra segmentazione batch e segmentazione in streaming viene effettuata dal sistema per ogni definizione di segmento, in base alla complessità e al costo della valutazione della regola del segmento. Puoi visualizzare il metodo di valutazione per ogni segmento nel **[!UICONTROL Metodo di valutazione]** dell’elenco dei segmenti.

![](assets/evaluation-method.png)

>[!NOTE]
>
>Se il **[!UICONTROL Metodo di valutazione]** La colonna non viene visualizzata, è necessario aggiungerla utilizzando il pulsante di configurazione in alto a destra nell’elenco.

Dopo aver definito per la prima volta un segmento, i profili vengono aggiunti al pubblico quando sono idonei.

Il backfill del pubblico dai dati precedenti può richiedere fino a 24 ore. Dopo che il pubblico è stato recuperato, viene costantemente aggiornato ed è sempre pronto per il targeting.
