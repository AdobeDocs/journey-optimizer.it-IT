---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione agli schemi
description: Scopri come utilizzare gli schemi di Adobe Experience Platform in Adobe Journey Optimizer
feature: Data Model, Datasets, Data Management
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: schemi, piattaforma, dati, struttura
exl-id: c2a8df2e-ff94-4f9a-a53e-bbf9f663cc81
source-git-commit: 70f647cf4e95c1152a5c16395b88b11a6b72865c
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 18%

---

# Introduzione agli schemi {#schemas-gs}

[!DNL Adobe Journey Optimizer] si basa su **schemi Adobe Experience Platform** per descrivere la struttura dei dati in modo coerente e riutilizzabile. Uno schema fornisce una definizione astratta di un oggetto reale (ad esempio una persona) e delinea quali dati includere in ogni istanza di tale oggetto (ad esempio nome, compleanno e così via). Quando i dati vengono acquisiti in Experience Platform, sono sempre strutturati in base a uno schema **XDM**.

## Schemi standard e relazionali

In Adobe Experience Platform sono disponibili due tipi di schemi:

* **Gli schemi standard** sono schemi gerarchici che utilizzano classi e gruppi di campi per acquisire dati di record o serie temporali.

  Uno schema standard è composto da:

   * Una **classe** (che definisce il comportamento dei dati: record o serie temporale).
   * Uno o più **gruppi di campi** (che aggiungono campi specifici allo schema).

  In Journey Optimizer, gli schemi standard vengono generalmente utilizzati per rappresentare **singole persone e i relativi attributi**, acquisire **interazioni di serie temporali** quali clic, acquisti o accessi e alimentare **Profilo cliente in tempo reale** per la segmentazione e la personalizzazione.

  ➡️ [Scopri come creare e configurare uno schema standard in questo video](#video-schema) (video)

* **Gli schemi relazionali** sono schemi piatti non gerarchici che non utilizzano classi o gruppi di campi. Vengono utilizzati per acquisire dati record per entità relazionali e vengono utilizzati principalmente in [!DNL Journey Optimizer] **campagne orchestrate**.

  Esempi di entità relazionali includono:
   * Prenotazioni, contratti o abbonamenti
   * Prodotti o cataloghi
   * Negozi, sedi o partner

  Con gli schemi relazionali, puoi inviare un messaggio per entità (ad esempio, per prenotazione, per abbonamento), creare segmenti basati sugli attributi di entità (ad esempio, categoria di prodotto, posizione del negozio) e migliorare l’indirizzabilità raggiungendo tutti i contatti collegati a un’entità.

  Funzionamento degli schemi relazionali:

   1. **Creare gli schemi manualmente o importarli tramite DDL**
   1. **Collega schemi** per definire le relazioni tra entità e persone (ad esempio, transazioni fedeltà collegate a membri, premi collegati a marchi).
   1. **Acquisisci dati** nel set di dati da origini supportate.

  ➡️ [Scopri come gestire schemi e set di dati relazionali](../orchestrated/gs-schemas.md)
➡️ [Introduzione alle campagne orchestrate](../orchestrated/gs-schemas.md)

## Video dimostrativo{#video-schema}

Scopri come creare uno schema standard, aggiungere gruppi di campi, creare e configurare gruppi di campi personalizzati.

>[!VIDEO](https://video.tv.adobe.com/v/334461?quality=12)

>[!MORELIKETHIS]
>
>* [Creare uno schema, un set di dati e acquisire dati per aggiungere profili di test in Journey Optimizer](../audience/creating-test-profiles.md)
>* [Panoramica del sistema XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}
>* [Best practice per la modellazione dati](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/best-practices.html?lang=it){target="_blank"}
>* [Creare uno schema tramite l’API del registro degli schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-api.html?lang=it){target="_blank"}
>* [Definire una relazione tra due schemi utilizzando l’editor di schemi](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/relationship-ui.html?lang=it){target="_blank"}
